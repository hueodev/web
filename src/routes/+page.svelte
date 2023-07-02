<script>
  import "../styles/global.scss";
  import Header from "../components/Header.svelte";
  import Info from "../components/Info.svelte";
  import Projects from "../components/Projects.svelte";
  import Links from "../components/Links.svelte";
</script>

<main>
  <Header />
  <Info />
  <Projects />
  <Links />
</main>

<style>
  main {
    margin: 4rem 2rem;
  }
</style>
