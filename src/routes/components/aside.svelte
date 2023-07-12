<script>
	import Menu from './aside/Menu.svelte'
</script>

<section class="section-aside">
    <div class="personal-details">
        <h1>Alvin Meroy</h1>
        <h2>Keyboard Tapper</h2>
    </div>

    <Menu />
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