<script>
    function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
        const all_nav_li = document.querySelectorAll('.nav-li');
        const parent_a = this.parentNode;
		if (!el) return;
        el.scrollIntoView({
            behavior: 'smooth',
            block: 'center',
        });
        all_nav_li.forEach( li => { li.classList.remove(`active`);}  );
        parent_a.classList.add('active');
     }
</script>

<div class="nav main-nav">
    <ul>
        <li class="nav-li active "><a href="#about" on:click|preventDefault={scrollIntoView}>About</a></li>
        <li class="nav-li "><a href="#experiences" on:click|preventDefault={scrollIntoView}>Experiences</a></li>
        <li class="nav-li "><a href="#case-studies" on:click|preventDefault={scrollIntoView}>Case Studies</a></li>
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
        padding: 1rem 0 1rem 2rem;
        position: relative;
        margin-bottom: 3rem;
    }

    .main-nav ul li::after {
        content: '';
        border-radius: 6px;
        width: 2px;
        height: 100%;
        max-height: 0;
        background-color: var(--accent);
        display: block;
        position: absolute;
        left: 0;
        top: 50%;
        transform: translateY(-50%);
        transition: all 0.3s linear;
    }

    .main-nav ul li.active::after {
        max-height: 6rem;
    }

    .main-nav ul li a {
        text-decoration: none;
        font-size: 1.4rem;
    }
</style>