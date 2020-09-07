<script context="module">
  export async function preload(page, session) {
    const res = await this.fetch('db/data.json')
    const smoothies = await res.json()
    return { smoothies }
  }
</script>

<script>
  export let smoothies
</script>

<svelte:head>
	<title>Products | Smoothies</title>
</svelte:head>

<ul class="recipes">
{#each smoothies as item}
  <li class="recipe">
    <img src={ item.img } alt="smoothie recipe icon">
    <h4>{ item.title }</h4>
    <p>{ item.desc }</p>
  </li>
  {/each}
</ul>