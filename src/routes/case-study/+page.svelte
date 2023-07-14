

<div id="wrap">
    <div class="container">
        <div class="aside">
            <h1>Case Study</h1>
        </div>
        <div class="content">
            <p>TODO...</p>
        </div>
    </div>
</div>

<style>
    .aside,
    .content {
        width: 100%;
        padding: 0;
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