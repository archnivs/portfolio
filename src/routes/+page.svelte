<script>
    import Aside from './components/aside.svelte';
    import Content from './components/content.svelte';
</script>

<div id="wrap">
    <div class="container">
        <div class="aside">
            <Aside />
        </div>
        <div class="content">
            <Content />
        </div>
    </div>
</div>

<style>
    .aside,
    .content {
        width: 100%;
        padding: 1rem;
        flex-grow: 1;
        flex-wrap: wrap;
    }

    @media screen and (min-width: 768px) {
        #wrap {
            margin-top: 4em;
        }
        .aside {
            width: 33%;
        }
        .content {
            width: 66%;
        }
    }
</style>