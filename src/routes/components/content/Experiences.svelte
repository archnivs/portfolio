<script>
	import ExperienceCard from './experience-card.svelte';

    const experiences = [
        {
            'company': 'Rock Solid Digital',
            'start_date': 'March 2022',
            'end_date': 'March 2023',
            'position': 'Fullstack Web Developer',
            'description': "- Develop a Wordpress theme using Sage (roots.io) as base theme and Advanced Custom Field to extend website functionality.<br>- Maintain a network of Hotel/Resort/Restaurant websites in WPMU installation.<br>- Maintain 2 plugins from WP Plugin repository developed by Rock Solid Digital.",
            'technology': ['WordPress', 'PHP', 'Javascript','ReactJS', 'CSS', 'HTML', 'Tailwind', 'Sage', 'Docker', 'Github'],
        },
        {
            'company': 'Apeirogon',
            'start_date': 'Aug 2020',
            'end_date': 'May 2021',
            'position': 'Web Developer',
            'description': '- Develop a Wordpress theme which is designed by the company’s web designer.<br>- Develop a custom plugin that will fill the gap of the features the website needs.<br>- Technical support for all the websites the company developed.',
            'technology': ['WordPress', 'PHP', 'Javascript', 'CSS', 'HTML', 'ACF Pro', 'Elementor Pro'],
        },
        {
            'company': 'Australian Writers Center',
            'start_date': 'Feb 2016',
            'end_date': 'May 2020',
            'position': 'Senior WordPress Developer',
            'description': '- Responsible for the development and additional feature of all their website build with Wordpress, namely: <br> > writerscentre.com.au, the company’s main website.<br> > learn.writerscentre.com.au, The company’s online learning hub<br> > discover.writerscentre.com.au, learning hub for teens and kids<br>- Technical support such as fixing bugs, feature changes and answering technical questions related to website development.',
            'technology': ['WordPress', 'PHP', 'Javascript', 'CSS', 'HTML', 'ACF Pro', 'BeaverBuilder', 'LearnDash', 'ReactJS'],
        },
        {
            'company': 'Englund Studio',
            'start_date': 'Feb 2016',
            'end_date': 'May 2020',
            'position': 'Web Developer',
            'description': '- Develop a Wordpress theme which is designed by the creative director.<br>- Develop a custom plugin that will fill the gap of the features the website needs.<br>- Technical support for all the websites the company developed.',
            'technology': ['WordPress', 'PHP', 'Javascript', 'CSS', 'HTML'],
        },
        {
            'company': 'WIDSIX',
            'start_date': 'Feb 2016',
            'end_date': 'May 2020',
            'position': 'Web Developer',
            'description': '- Develop a Wordpress theme which is designed by the company’s web designer.<br- Develop a custom plugin that will fill the gap of the features the website needs.',
            'technology': ['WordPress', 'PHP', 'Javascript', 'CSS', 'HTML'],
        },
    ];
</script>

<section id="experiences" class="section-wrapper section-experiences">
    <h3 class="section-title">Experiences</h3>
   
    {#each experiences as experience}
        <ExperienceCard {experience} />
    {/each}
</section>