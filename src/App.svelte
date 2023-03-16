<script>
  import Status from "./lib/Status.svelte";
  import Header from "./lib/Header.svelte";
  import TechStack from "./lib/TechStack.svelte";
  import Contact from "./lib/Contact.svelte";
</script>

<main>
  <Header/>
  <TechStack/>
  <Contact/>
  <Status/>
</main>

<style>
@import url("https://api.fontshare.com/v2/css?f[]=satoshi@1,900,700,500,301,701,300,501,401,901,400,2&display=swap");

:global(*) {
  font-family: "Satoshi";
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
