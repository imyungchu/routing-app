<template>
  <main>
    <div class='links'>
      <RouterLink class="nav-link" active-class='active' to='/'>Home</RouterLink>
      <RouterLink class="nav-link" active-class='active' to='/about'>About</RouterLink>
    </div>
    <RouterView />
  </main>
</template>

<style scoped>
  .links {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    background-color: #333; 
  }

  .nav-link {
    margin: 0 10px;
    text-decoration: none;
    color: #fff; 
    font-weight: bold;
    transition: color 0.3s ease;
  }

  .nav-link:hover {
    color: #00ff00; 
  }

  .active {
    color: #00ff00; 
  }
</style>
