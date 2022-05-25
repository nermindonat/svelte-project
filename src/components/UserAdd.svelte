<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  const cancelHandler = () => {
    dispatch("toggleTable");
  };
</script>

<div class="container1">
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
  <form class="row">
    <div class="col-6">
      <label for="fname">User Name</label>
      <input
        type="text"
        id="fname"
        name="firstname"
        placeholder="Your name.."
      />
    </div>

    <div class="col-6">
      <label for="lname">User Lastname</label>
      <input
        type="text"
        id="lname"
        name="lastname"
        placeholder="Your last name.."
      />
    </div>

    <div class="col-6">
      <label for="email">Email</label>
      <input type="text" id="email" name="email" placeholder="Your email.." />
    </div>

    <div class="col-6">
      <label for="birthday">Birthday</label>
      <input type="date" id="birthday" name="birthday" />
    </div>
  </form>

  <div class="buttons">
    <button class="button-cancel" on:click={cancelHandler}>Cancel</button>
    <button class="button-save">Save</button>
  </div>
</div>

<style>
  .container1 {
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

  .row {
    margin: 20px 20px 0 20px;
    padding: 10px;
  }

  form {
    padding: 10px;
  }

  input[type="text"] {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
  }

  input[type="date"] {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
  }

  input:focus {
    outline: none;
  }

  form label {
    display: block;
    font-size: 15px;
    font-weight: 500;
  }

  .buttons {
    margin-right: 40px;
    display: flex;
    justify-content: flex-end;
  }

  .button-save {
    background-color: #008cba;
    font-size: 15px;
    font-weight: 500;
    margin-left: 10px;
    border-radius: 5px;
    color: white;
    text-transform: uppercase;
  }

  .button-cancel {
    background-color: #f44336;
    font-size: 15px;
    border-radius: 5px;
    color: white;
    text-transform: uppercase;
    font-weight: 500;
  }
</style>
