<script>
	import { page } from '$app/stores';
	let status = $page.status;
</script>

<div class="container">
    <h1>{status}</h1>
    <p>{$page.error?.message}</p>
</div>


<style lang="scss">
    .container {
        height: calc(100vh - 70px);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    h1 {
        font-size: 3.4rem;
    }
</style>