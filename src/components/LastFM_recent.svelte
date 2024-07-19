<script lang="ts">
    import { onMount } from 'svelte';

    interface Track {
		time_str: string;
		artist: string;
        track: string;
        playback_date: string;
    }

    let tracks: Track[] = [];

    function fetchRecentTracks(username: string, number: number) {
        const url = `https://pbg7nrxuse.execute-api.us-west-1.amazonaws.com/dev/recent-tracks?username=${encodeURIComponent(username)}&number=${number}`;

        fetch(url)
            .then(response => {
                if (!response.ok) {
                    throw new Error('Failed to fetch data');
                }
                return response.json();
            })
            .then((data: any[]) => {
                tracks = data.map(track => ({
                    track: track.track,
                    artist: track.artist,
                    time_str: track.time_str,
                    playback_date: track.playback_date
                }));
            })
            .catch(error => {
                console.error(error);
            });
        }

    onMount(() => {
        fetchRecentTracks('arnavsurve', 10); // Fetch top 5 tracks for 'arnavsurve'
    });
</script>


<div id="tracks-container" class="border-2 border-slate-500 rounded-md">
    {#each tracks as track}
        <div class="track text-sm p-2">
            <h3>{track.artist} - [{track.track}]</h3>
            <p class="text-xs text-slate-500">{track.time_str}</p>
        </div>
    {/each}
</div>
