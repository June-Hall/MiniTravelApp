<template>
  <nav id="nav">
    <ul class="nav-links">
      <li class="links">
        <router-link to="/"> Home </router-link>
      </li>
      <li>
        
      </li>
    </ul>
  </nav>
</template>

<style scoped>
#nav {
  display: flex;
  justify-content: center;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 0 10px;
}

nav a.router-link-exact-active {
  color: #ab26ab;
}
</style>
