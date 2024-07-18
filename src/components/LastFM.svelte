<script lang="ts">
    import { onMount } from 'svelte';

    interface Track {
        title: string;
        artist: string;
        playCount: number;
    }

    let tracks: Track[] = [];

    function fetchTopTracks(username: string, number: number) {
        const url = `https://pbg7nrxuse.execute-api.us-west-1.amazonaws.com/dev/top-tracks?username=${encodeURIComponent(username)}&number=${number}`;

        fetch(url)
            .then(response => {
                if (!response.ok) {
                    throw new Error('Failed to fetch data');
                }
                return response.json();
            })
            .then((data: any[]) => {
                tracks = data.map(track => ({
                    title: track.title,
                    artist: track.artist,
                    playCount: track['play-count']
                }));
            })
            .catch(error => {
                console.error(error);
            });
        }

    onMount(() => {
        fetchTopTracks('arnavsurve', 10); // Fetch top 5 tracks for 'arnavsurve'
    });
</script>


<div id="tracks-container" class="border-2 border-slate-500 rounded-md">
    {#each tracks as track}
        <div class="track text-sm p-2">
            <h3>{track.artist} [{track.title}]</h3>
            <p class="text-xs text-slate-500">{track.playCount} plays</p>
        </div>
    {/each}
</div>
