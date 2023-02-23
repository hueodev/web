<script>
  import Header from "./Components/Header.svelte";
  import TechStack from "./Components/TechStack.svelte";
  import Contact from "./Components/Contact.svelte";
</script>

<main>
  <Header/>
  <TechStack/>
  <Contact/>
</main>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&display=swap');

:global(*) {
  font-family: "Roboto Condensed" !important;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:global(body) {
  background-color: rgb(24, 24, 27);
  color: rgb(255, 255, 255);
}

:global(:root) {
  color-scheme: dark;
}
</style>
