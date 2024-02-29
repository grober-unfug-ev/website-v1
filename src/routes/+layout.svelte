<script>
    import "../app.css";
    import logo from '$lib/assets/logo.png';
    import {Navbar, NavBrand, NavHamburger, NavLi, NavUl} from "flowbite-svelte";
    import { Footer, FooterCopyright, FooterLinkGroup, FooterLink } from 'flowbite-svelte';

    $: currentYear = new Date().getFullYear();
</script>

<Navbar class="bg-purple-950 drop-shadow-lg">
    <NavBrand href="/">
        <img src="{logo}" alt="logo" class="h-12" />
        <h1 class="ml-4 text-xl text-purple-100">Grober Unfug e.V.</h1>
    </NavBrand>
    <NavHamburger class="text-purple-300 hover:text-purple-200 hover:bg-purple-800" />
    <NavUl classUl="bg-purple-950">
        <NavLi class="text-[1.1rem] text-purple-300 hover:text-purple-200 hover:text-purple-200 hover:bg-purple-700" href="/">Home</NavLi>
        <NavLi class="text-[1.1rem] text-purple-300 hover:text-purple-200 hover:text-purple-200 hover:bg-purple-700" href="/downloads">Downloads</NavLi>

        <span class="border-l-2 border-purple-900"></span>

        <NavLi class="text-purple-300 hover:text-purple-200 hover:bg-purple-900 flex flex-row gap-8" href="/downloads">
            <a href="https://www.instagram.com/grober_unfug_ev" target="_blank">
                <svg class="h-6 w-6 fill-purple-400 hover:fill-purple-300" viewBox="0 0 448 512" xmlns="http://www.w3.org/2000/svg"><g transform="translate(224 256)" transform-origin="112 0"><g transform="translate(0,0) scale(1.15,1.15)"><path d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z" transform="translate(-224 -256)"></path></g></g></svg>
            </a>
            <a href="https://www.facebook.com/PsyParkBonn" target="_blank">
                <svg class="h-6 w-6 fill-purple-400 hover:fill-purple-300" viewBox="0 0 512 512" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg"><g transform="translate(256 256)" transform-origin="128 0"><g transform="translate(0,0) scale(1,1)"><path d="M512 256C512 114.6 397.4 0 256 0S0 114.6 0 256C0 376 82.7 476.8 194.2 504.5V334.2H141.4V256h52.8V222.3c0-87.1 39.4-127.5 125-127.5c16.2 0 44.2 3.2 55.7 6.4V172c-6-.6-16.5-1-29.6-1c-42 0-58.2 15.9-58.2 57.2V256h83.6l-14.4 78.2H287V510.1C413.8 494.8 512 386.9 512 256h0z" transform="translate(-256 -256)"></path></g></g></svg>
            </a>
        </NavLi>
    </NavUl>
</Navbar>

<main class="h-screen bg-purple-900 text-purple-100 p-4">
    <slot />
</main>

<Footer class="bg-neutral-900 p-4">
    <FooterCopyright spanClass="block text-sm text-gray-500 text-center" href="/" by="Grober Unfug e.V." year={currentYear} copyrightMessage="" />
    <FooterLinkGroup ulClass="pt-2 sm:pt-4 justify-center flex flex-wrap items-center mt-3 text-sm text-gray-500">
        <FooterLink href="/imprint">Impressum</FooterLink>
        <FooterLink href="/contact">Kontakt</FooterLink>
        <FooterLink href="/downloads">Downloads</FooterLink>
    </FooterLinkGroup>
</Footer>