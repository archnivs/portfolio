<script>
	import Menu from './aside/Menu.svelte';
    import myCV from '$lib/Alvin-Meroy-CV-.pdf';
</script>

<section class="section-aside">
    <div class="personal-details">
        <h1>Alvin Meroy</h1>
        <h2>Keyboard Tapper</h2>
    </div>

    <Menu />

    <a class="btn-cv btn" target="_blank" href="{myCV}">Download my CV</a>
</section>

<style>
    @media screen and (min-width: 768px) {
        .section-aside {
            position: fixed;
            width: 30%;
        }

        .personal-details {
            margin-bottom: 6rem;
        }
    }
</style>