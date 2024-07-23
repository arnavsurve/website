<script>
    import Header from "../components/Header.svelte";
    import Prose from "../components/Prose.svelte";
    import StyleLink from "../components/StyleLink.svelte";
</script>

<Header />

<div class="m-4 font-mono sm:flex md:flex lg:flex justify-between">
    <div class="m-2">
            <Prose>
                I am a third-year student at California State Univerity, Sacramento pursuing a Bachelor's degree in Computer Science.
                <br><br>
                Currently, Linux and DevOps engineering have been of key interest to me, and I have been working through this <StyleLink url="https://roadmap.sh/devops">DevOps Roadmap</StyleLink>. I am also studying for the <StyleLink>AWS Cloud Practitioner</StyleLink> certification with plans to obtain a <StyleLink>SysOps Administrator - Associate</StyleLink> certification as well.
                <br><br>
                I am focused on developing a strong foundation in Go and Python programming, as well as familiarizing myself with the RHEL ecoystem with a bare metal install of Fedora Linux. I have experience with both Debian (apt) and RHEL (dnf) based distributions.
            </Prose>
    
            <br>
    
            <div class="font-mono">
                <h1 class="text-xl">
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
