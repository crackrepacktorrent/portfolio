<script lang="ts">
	import '../app.css';
	let { children } = $props();
	import arepa from "$lib/arepa.png";
	import arepa2 from "$lib/arepa2.png";
	import arepa3 from "$lib/arepa3.png";
	import { crossfade } from 'svelte/transition';
	import { page } from '$app/state';
</script>

<div class="my-auto grid grid-cols-[25vh_auto_25vh] gap-4 w-[95vw]">
    <div class="">
        <h1 class="pb-10 font-black  text-5xl">buh-!</h1>
        <h1 class="pb-10">whoami?</h1>
        <img src={arepa2} alt="an arepa with a face!" class="pb-10">
        <p class="pb-10">
            josé davila-ciullo (they/them)! I'm a CS student (systems track) at stanford, some of my interests include:
        </p>
        <ul class="list-disc pl-6 pb-10">
            <li>
                piracy
            </li>
            <li>
                game dev/design (esp with bevy)
            </li>
			<li>
				videogames
			</li>
			<li>
				internet privacy
			</li>
			<li>
				computer/network security
			</li>
            <li>
                p2p protocols
            </li>
            <li>
                cryptography
            </li>

			<li>
				anarchism
			</li>
            <li>
                critical theory
            </li>
        </ul>
        <p class="pb-10">reach me at...</p>
        <ul class=" list-disc pl-6">
            <li>ihackpigs&lt;at&gt;protonmail&lt;dot&gt;com</li>
            <li>josedav&lt;at&gt;stanford&lt;dot&gt;edu</li>
        </ul>
    </div>
    <div class="">
        {@render children()}
    </div>
    <div class="text-right" dir="rtl">
        <ul class="list-disc pr-6">
			<li>
				<a href="/" class={page.url.pathname === "/" ? "active" : ""}>home</a>
			</li>
            <li>
                <a href="/projects" class={page.url.pathname === "/projects" ? "active" : ""}>projects</a>
            </li>
            <li>
                <a href="/art" class={page.url.pathname === "/art" ? "active" : ""}>art</a>
            </li>
        </ul>
    </div>
    <div class=" p-2 col-span-3 text-center">
    </div>
</div>

<style>
	.active {
		background-color: yellow;
	}
</style>