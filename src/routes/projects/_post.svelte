<svelte:head>
  <title>{title} | cika.info </title>
  <meta property="og:title" content={title} />
</svelte:head>

<!-- _post.svelte -->
<script>
    export let title
    export let date
  </script>
  
  <h1>{title}</h1>
  
  <p>Published: {date}</p>
  
  <slot />