<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  const cancelHandler = () => {
    dispatch("toggleTable");
  };

  const showSidebar = () => {
    dispatch("toggleSidebar")
  }
</script>

<div class="row2">
  <navbar class="navbar">
    <button class="openbtn" on:click={showSidebar}>☰</button>
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
  .row2 {
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
