<script>
    import Fa from 'svelte-fa';
    import { faEnvelope } from '@fortawesome/free-solid-svg-icons';
    import { 
        faGithub,
        faCodepen,
        faLinkedin 
    } from '@fortawesome/free-brands-svg-icons'; 


    const social_media_links = [
        {
            'label': 'Codepen',
            'icon': faCodepen,
            'link': 'https://codepen.io/archnivs',
        },
        {
            'label': 'Github',
            'icon': faGithub,
            'link': 'https://github.com/archnivs',
        },
        {
            'label': 'LinkedIn',
            'icon': faLinkedin,
            'link': 'https://www.linkedin.com/in/alvinmeroy/',
        },
        {
            'label': 'Email',
            'icon': faEnvelope,
            'link': 'mailto:archnivs@gmail.com',
        },
    ];
</script>

<div class="social-media-links">
    {#each social_media_links as sm}
    <a href={sm.link} class="sm-link" target="_blank">
        <span class="sm-icon sm-{sm.label}">
        <Fa 
            icon={sm.icon} 
            size="2x" />
        </span>
    </a>
    {/each}
</div>

<style>
    .social-media-links {
        margin-top: 4rem;
        display: flex;
        gap: 2.6rem;
    }
</style>