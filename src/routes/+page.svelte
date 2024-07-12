<script>
    import Header from "../components/Header.svelte";
    import Prose from "../components/Prose.svelte";
    import Resume from "../components/Resume.svelte";
</script>

<Header />

<div class="flex">
    <div class="m-4">
        <Prose>
            I am a third-year student at California State Univerity, Sacramento pursuing a Bachelor's degree in Computer Science.
            <br><br>
            Currently, Linux and DevOps engineering have been of key interest to me, and I have been working through this <a href="https://roadmap.sh/devops" class="text-slate-500 hover:underline">DevOps Roadmap</a>. 
            <br><br>
            I am focused on developing a strong foundation in Go and Python programming, as well as familiarizing myself with the RHEL ecoystem with a bare metal install of Fedora Linux. I have experience with both Debian (apt) and RHEL (dnf) based distributions.
        </Prose>

        <br>

        <div class="font-mono">
            <h1 class="text-xl font-mono">
                this summer I am:
            </h1>

            <ul class="text-sm list-disc p-2">
                <li>Interning at Milgard Manufacturing, IT DevOps in Tacoma, WA</li>
                <li>Conducting infrasound research under the NASA California Space Grant Consortium</li>
                <li>Taking MATH410 (Intro to Linear Algebra) at American River College</li>
            </ul>
        </div>
    </div>
</div>