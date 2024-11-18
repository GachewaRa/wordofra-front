<!-- HighlightCard.svelte -->
<script>
  export let title;
  export let description;
  export let image;
  export let link;
</script>

<div class="highlight-card">
  <img src={image} alt={title} class="highlight-image" />
  <div class="highlight-content">
    <h3>{title}</h3>
    <p>{description}</p>
    <Link to={link} class="read-more">Read More →</Link>
  </div>
</div>
