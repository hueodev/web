<script>
  import Header from "./Components/Header.svelte";
  import TechStack from "./Components/TechStack.svelte";
  import Contact from "./Components/Contact.svelte";
</script>

<svelte:head>
  <meta property="og:type" content="website">
  <meta property="og:site_name" content="ogooo.dev">
  <meta property="og:title" content="Ogooo#7072">
  <meta property="og:description" content="Ogooo - Frontend developer">
  <meta property="og:image" content="https://avatars.githubusercontent.com/u/78303660?v=4">
  <meta content="#202225" data-react-helmet="true" name="theme-color" />
</svelte:head>

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
