<script>
  import { onMount } from "svelte";

  let userPresence = {};

  async function fetchPresence() {
    const res = await fetch("https://api.lanyard.rest/v1/users/420661585007083520");
    if (res.ok) {
      userPresence = await res.json();
    }
  }

  onMount(() => {
    fetchPresence();
    setInterval(fetchPresence, 10000);
  });
</script>

{#if userPresence.data}
	{#if userPresence.data.discord_status === "online" || userPresence.data.discord_status === "dnd" || userPresence.data.discord_status === "idle"}
		<span class="online">Currently Online</span>
	{:else if userPresence.data.discord_status === "offline"}
		<span class="offline">Currently Offline</span>
	{/if}
{/if}

{#if !userPresence.data}
	<span>Currently Loading</span>
{/if}

<style lang="scss">
  span {
    font-size: 0.94rem;
    color: whitesmoke;
  }

  .online::after {
    content: "";
    display: inline-block;
    vertical-align: middle;
    margin: 0 0 0 0.3rem;
    height: 0.6rem;
    width: 0.6rem;
    border-radius: 100%;
    background-color: rgb(80, 163, 97);
  }

  .offline::after {
    content: "";
    display: inline-block;
    vertical-align: middle;
    margin: 0 0 0 0.3rem;
    height: 0.6rem;
    width: 0.6rem;
    border-radius: 100%;
    background-color: rgb(129, 132, 141);
  }
</style>
