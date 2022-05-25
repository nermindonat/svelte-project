<script>
	import Sidebar from "./components/Sidebar.svelte";
	import Table from "./components/Table.svelte";
	import UserAdd from "./components/UserAdd.svelte";

	let showTable = true;

	const  toggleTable = () => {
		showTable = !showTable
	}

</script>

{#if showTable}
  <Table on:toggleTable={toggleTable}/>
{:else}
  <UserAdd on:toggleTable={toggleTable}/>
{/if}

<Sidebar/>
