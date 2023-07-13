<script>
    import Fa from 'svelte-fa';
    import { faDownload } from '@fortawesome/free-solid-svg-icons';
	import Menu from './aside/Menu.svelte';
	import SocialMedia from './aside/Social-Media.svelte';
    import myCV from '$lib/Alvin-Meroy-CV-.pdf';
</script>

<section class="section-aside">
    <div class="personal-details">
        <h1>Alvin Meroy</h1>
        <h2>Web Developer</h2>
    </div>

    <Menu />

    <a class="btn-cv btn" target="_blank" href="{myCV}">Download my CV <Fa icon={faDownload} translateX={0.5} size="lg" /></a>

    <SocialMedia />
</section>

<style>
    .section-aside {
        text-align: center;
    }

    .btn-cv {
        display: none;
    }

    @media screen and (min-width: 768px) {
        .section-aside {
            text-align: inherit;
            position: fixed;
            width: 30%;
        }

        .personal-details {
            margin-bottom: 6rem;
        }

        .btn-cv {
            display: inline-block;
        }
    }
</style>