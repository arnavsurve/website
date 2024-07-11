<script>
    import Header from "../components/Header.svelte";
    import Prose from "../components/Prose.svelte";
</script>

<Header />

<div class="flex">
    <div class="">
        <Prose>
            I am a third-year student at California State Univerity, Sacramento pursuing a Bachelor's degree in Computer Science.
            <br><br>
            Currently, Linux and DevOps engineering have been of key interest to me, and I am currently working through this <a href="https://roadmap.sh/devops" class="text-slate-400 hover:underline">DevOps Roadmap</a>. 
            <br><br>
            I am focused on developing a strong foundation in Go and Python programming, as well as familiarizing myself with the RHEL ecoystem with a bare metal install of Fedora Linux. I have experience with both Debian (apt) and RHEL (dnf) based distributions.
        </Prose>

        <!-- I am particularly interested in Linux kernel development. Recently, I have been involving myself with the <a href="https://asahilinux.org/" class="text-slate-400 hover:underline">Asahi Linux</a> project. This is a fork of the Linux kernel with the mission of bringing a polished Linux experience to Apple Silicon. I am currently working on a driver for M2 Pro Macbook Pro webcam support. -->


        <div class="font-mono p-4">
            <h1 class="text-xl font-mono">
                this summer I am:
            </h1>

            <ul class="text-sm list-disc p-2">
                <li>Interning at Milgard Manufacturing, IT DevOps in Tacoma, WA</li>
                <li>Conducting infrasound research under the NASA California Space Grant Consortium</li>
                <li>Taking MATH410 (Intro to Linear Algebra) at American River College</li>
            </ul>

            <br>

            <!-- <h1 class="text-xl"> -->
            <!--     planned -->
            <!-- </h1> -->

        </div>
    </div>
</div>