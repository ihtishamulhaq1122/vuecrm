<template>
    <nav class="navbar">
      <div class="navbar-logo">
        <img src="logo.png" alt="Logo" />
      </div>
      <div class="navbar-search">
        <input type="text" placeholder="Search" />
        <button>Search</button>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'NAVBARMENU',
  };
  </script>
  
  <style>
  .navbar {
    background-color: rgb(17,16,29);
    color: #fff;
    padding: 10px;
    display: flex;
    justify-content: space-between;
  }
  
  .navbar-logo img {
    height: 30px;
  }
  
  .navbar-search {
    display: flex;
    align-items: center;
  }
  
  .navbar-search input {
    margin-right: 10px;
  }
  </style>
  