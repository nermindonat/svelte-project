<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  const addUserHandler = () => {
    dispatch("toggleTable");
  };
</script>

<div class="container2">
  <navbar class="navbar">
    <span class="icon"
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-x-lg"
        viewBox="0 0 16 16"
      >
        <path
          d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8 2.146 2.854Z"
        />
      </svg></span
    >
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
  .container2 {
    margin-left: 200px;
  }
  .navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f7f6fb;
    height: 40px;
  }

  .navbar span {
    padding-right: 15px;
    padding-left: 15px;
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
    padding-left: 10px;
    padding-right: 10px;
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
</style>
