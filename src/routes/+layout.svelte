<script>
    import "../app.css";
    import logo from '$lib/assets/logo.png';
    import Fa from 'svelte-fa'
    import { faBars } from '@fortawesome/free-solid-svg-icons'
    import { faInstagram, faFacebook } from '@fortawesome/free-brands-svg-icons'
</script>

<nav class="py-2 px-4 sm:px-16 flex flex-row bg-purple-950 justify-between drop-shadow-lg">
    <!-- Logo + Name -->
    <div class="flex flex-row gap-2 items-center">
        <img src="{logo}" alt="logo" class="h-12" />
        <h1 class="text-xl text-purple-100">Grober Unfug e.V.</h1>
    </div>

    <!-- Links and Socials -->
    <div class="flex flex-row items-center">
        <!-- Mobile -->
        <div class="block sm:hidden">
            <!-- Hamburger -->
            <button class="block">
                <Fa icon={faBars} size="lg" color="#ffffff" />
            </button>
        </div>

        <!-- Desktop -->
        <div class="hidden sm:flex flex-row text-purple-300">
            <!-- Links -->
            <div class="flex flex-row">
                <a href="/" class="px-4 hover:text-purple-200">Home</a>
                <a href="/downloads" class="px-4 hover:text-purple-200">Downloads</a>
            </div>

            <!-- Socials -->
            <div class="flex flex-row ml-6 pl-6 border-l-2 border-purple-900">
                <a href="https://www.instagram.com/grober_unfug_ev" target="_blank" class="px-4">
                    <Fa icon={faInstagram} size="lg" color="#c084fc" scale="1.15" />
                </a>
                <a href="https://www.facebook.com/PsyParkBonn" target="_blank" class="px-4">
                    <Fa icon={faFacebook} size="lg" color="#c084fc" />
                </a>
            </div>
        </div>
    </div>

</nav>

<main class="h-screen bg-purple-900 text-purple-100 p-4">
    <slot />
</main>