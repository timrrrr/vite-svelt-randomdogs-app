<script lang="ts">
  // import svelteLogo from './assets/svelte.svg'
  // import Counter from './lib/Counter.svelte'
  import DogFetcher from './lib/DogFetcher.svelte'
  import About from './lib/About.svelte';
  import Content from './lib/Content.svelte';
  import Header from './lib/Header.svelte';
</script>

<main>
  <Header></Header>
  <div class = content>
    <DogFetcher></DogFetcher>
    <About></About>
  </div>
</main>

<style>
</style>