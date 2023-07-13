<script>
    export let experience = [];
</script>

<div class="experience-card card">
    <h5>{experience.company}</h5>
    <h6>
        <span class="position">{experience.position}</span> &#x2022; 
        <span class="work-duration">{experience.start_date} - {experience.end_date}</span>
    </h6>
    <div class="description">
        {@html experience.description}
    </div>
    <div class="technology">
        {#each experience.technology as item}
            <span class="tech-item">{item}</span>
        {/each}
    </div>
</div>

<style>
    .experience-card h5 {
        margin-bottom: 1rem;
    }

    .experience-card h6 {
        margin-bottom: 1rem;
        font-size: 1.2rem;
        font-style: italic;
    }

    .experience-card .description {
        margin-bottom: 1.6rem;
        line-height: 1.6;
    }

    .technology {
        display: flex;
        flex-wrap: wrap;
        justify-content:flex-start;
        gap: 0.75rem;
    }

    .technology .tech-item {
        padding: 0.4rem 1.5rem;
        background-color: var(--accent-2);
        color: var(--primary-color);
        border-radius: 20px;
        font-size: 14px;    
    }
</style>