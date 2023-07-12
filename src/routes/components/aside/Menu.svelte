<script>
    import { onMount } from 'svelte';

    function setActiveNav(all_nav_li, active_li) {
        all_nav_li.forEach( li => { li.classList.remove(`active`);}  );
        active_li.classList.add('active');
    }
    function scrollIntoView({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
        const all_nav_li = document.querySelectorAll('.nav-li');
        const parent_a = this.parentNode;
		if (!el) return;
        el.scrollIntoView({
            behavior: 'smooth',
            block: 'start',
        });
        //setActiveNav(all_nav_li, parent_a);
     }

    onMount(()=> {
        window.onscroll = () => {
            const sections = document.querySelectorAll(".section-wrapper");
            const all_nav_li = document.querySelectorAll('.nav-li');
            sections.forEach((section) => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - sectionHeight / 3) {
                    const el = document.querySelector("#nav-" + section.getAttribute("id"));
                    setActiveNav(all_nav_li, el);
                }
            });
        }
    })

    
</script>



<div class="nav main-nav">
    <ul>
        <li id="nav-about" class="nav-li active "><a href="#about" on:click|preventDefault={scrollIntoView}>About</a></li>
        <li id="nav-experiences" class="nav-li "><a href="#experiences" on:click|preventDefault={scrollIntoView}>Experiences</a></li>
        <li id="nav-case-studies" class="nav-li "><a href="#case-studies" on:click|preventDefault={scrollIntoView}>Case Studies</a></li>
    </ul>
</div> 

<style>
    .main-nav {
        margin-bottom: 5rem;
        display: none;
    }

    @media screen and (min-width: 768px) {
        .main-nav {
            display: block;
        }
    }

    .main-nav ul {
        list-style: none;
        margin: 0;
        padding: 0;
        width: 100%;
    }

    .main-nav ul li {
        padding: 1rem 0 1rem 0;
        position: relative;
        margin-bottom: 3rem;
        transition: all 200ms linear;
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
        transition: all 300ms linear;
    }

    .main-nav ul li.active {
        padding-left: 2rem;
    }

    .main-nav ul li.active::after {
        max-height: 6rem;
    }

    .main-nav ul li a {
        text-decoration: none;
        font-size: 1.4rem;
    }
</style>