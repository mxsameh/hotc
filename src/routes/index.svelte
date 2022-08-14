<script>
  import Footer from "$lib/components/Footer.svelte";
  import Header from "$lib/components/Header.svelte";
  import Hero from "$lib/home/Hero.svelte";
  import Help from "$lib/components/Help.svelte";
  import Developers from "$lib/home/Developers.svelte";
  import Projects from "$lib/home/Projects.svelte";
  import Services from "$lib/home/Services.svelte";
</script>

<Header/>
<Hero/>

<div class="container">
  <Services/>
  <Projects/>
  <Developers/>
  <Help/>
</div>

<Footer/>