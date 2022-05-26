<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  
  const addUserHandler = () => {
    dispatch("toggleTable");
  };

  const showSidebar = () => {
    dispatch("toggleSidebar")
  }

  
</script>

<div class="row1">
  <navbar class="navbar">
    <button class="openbtn" on:click={showSidebar}>☰</button>
    <span class="text">Admin Panel</span>
  </navbar>
  <div class="table-wrapper">
    <header class="header">
      <span class="header-text">Users</span>
      <button class="button" on:click={addUserHandler}>Add + </button>
    </header>
    <table class="content-table">
      <tr>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Email</th>
        <th>Birthdate</th>
      </tr>
      <tr>
        <td>Peter</td>
        <td>Griffin</td>
        <td>peter@gmail.com</td>
        <td>Mon Jul 15</td>
      </tr>
      <tr>
        <td>Lois</td>
        <td>Griffin</td>
        <td>lois@gmail.com</td>
        <td>Mon Jul 15</td>
      </tr>
      <tr>
        <td>Joe</td>
        <td>Swanson</td>
        <td>joe@gmail.com</td>
        <td>Mon Jul 15</td>
      </tr>
      <tr>
        <td>Cleveland</td>
        <td>Brown</td>
        <td>cleveland@gmail.com</td>
        <td>Mon Jul 15</td>
      </tr>
    </table>
    <hr />
  </div>
</div>

<style>
  .row1 {
    width: 100%;
    
  }
  .navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f7f6fb;
  }


  .text {
    font-size: 15px;
    font-weight: bold;
  }

  .table-wrapper {
    margin-top: 10px;
    margin-left: 20px;
    margin-right: 20px;
    border: 1px solid #bab8c0;
  }

  .header {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f7f6fb;
    height: 40px;
  }

  .header span {
    padding-right: 15px;
    padding-left: 15px;
  }

  .button {
    margin: 10px;
    padding-bottom: 8px;
    background-color: green;
    color: white;
    font-size: small;
    font-weight: bold;
    border-radius: 5px;
  }
  .content-table {
    margin-top: 10px;
    width: 100%;

  }

  th,
  td {
    padding: 8px;
    text-align: left;
    border-bottom: 1px solid #ddd;
  }

  tr:hover {
    background-color: #d6eeee;
  }

  hr {
    margin-right: 10px;
    margin-left: 10px;
  }

  .openbtn {
  font-size: 20px;
  cursor: pointer;
  background-color: #f7f6fb;
  color: black;
  font-weight: bold;
  border: none;
}

.openbtn:hover {
  color: rgb(48, 37, 37);
}

</style>
