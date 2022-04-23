<script>
// @ts-nocheck
// ts will only be supported for mdsvex v1.0+

    export let title
    export let date
    export let categories
</script>

<h1>{title}</h1>
<p>Published: {date}</p>

{#if categories.length}
<aside>
    <h2>Posted in:</h2>
    <ul>
        {#each categories as category}
        <li>
            <a href="/blog/categories/{category}">
                {category}
            </a>
        </li>
        {/each}
    </ul>
</aside>
{/if}

<slot />