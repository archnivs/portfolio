<script>
    function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
        const all_nav_li = document.querySelectorAll('.nav-li');
        const parent_a = this.parentNode;
		if (!el) return;
        el.scrollIntoView({
            behavior: 'smooth',
        });
        all_nav_li.forEach( li => { li.classList.remove(`active`);}  );
        parent_a.classList.add('active');
     }
</script>

<div class="nav main-nav">
    <ul>
        <li class="nav-li active "><a href="#about" on:click|preventDefault={scrollIntoView}>About</a></li>
        <li class="nav-li "><a href="#experiences" on:click|preventDefault={scrollIntoView}>Experience</a></li>
        <li class="nav-li "><a href="#case-studies" on:click|preventDefault={scrollIntoView}>Case Study</a></li>
    </ul>
</div> 

<style>
    .main-nav ul {
        list-style: none;
        margin: 0;
        padding: 0;
        width: 100%;
    }

    .main-nav ul li {
        padding: 2rem 0;
        position: relative;
    }

    .main-nav ul li.active::after {
        content: '';
        border-width: 32px 24px 32px 10px;
        border-color: Transparent var(--accent) transparent transparent;
        border-style: solid;
        display: block;
        position: absolute;
        right: 0;
        top: 50%;
        transform: translateY(-50%);
        transition: all 0.3s linear;
    }

    .main-nav ul li a {
        text-decoration: none;
        font-size: 1.4rem;
    }
</style>