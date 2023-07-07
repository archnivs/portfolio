<script>
	import Nav from './aside/Nav.svelte'
</script>

<section class="section-aside">
    <div class="personal-details">
        <h1>Alvin Meroy</h1>
        <h3>Keyboard Tapper</h3>
    </div>

    <Nav />
</section>

<style>
    @media screen and (min-width: 768px) {
        .section-aside {
            position: fixed;
            width: 30%;
        }
    }
</style>