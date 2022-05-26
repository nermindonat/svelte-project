<script>
  import Sidebar from "./components/Sidebar.svelte";
  import Table from "./components/Table.svelte";
  import UserAdd from "./components/UserAdd.svelte";

  let showTable = true;

  let showSidebar = true;

  const toggleTable = () => {
    showTable = !showTable;
  };

  const toggleSidebar = () => {
    showSidebar = !showSidebar;
  };
</script>

<div class="row">
  {#if showSidebar}
    <Sidebar on:toggleSidebar={toggleSidebar} />
  {/if}
  <main>
    {#if showTable}
      <Table on:toggleTable={toggleTable} on:toggleSidebar={toggleSidebar} />
    {:else}
      <UserAdd on:toggleTable={toggleTable} />
    {/if}
  </main>
</div>

<style>
  .row {
    height: 100vh;
    margin: 0;
  }

  main {
    display: flex;
    flex: 1;
  }
</style>
