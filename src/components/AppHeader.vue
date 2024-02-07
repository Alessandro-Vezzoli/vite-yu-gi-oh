<template>
  <header>
    <div class="container">
      <nav>
        <ul class="nav-list">
          <li><img class="img" src="/img/logo-yu-gi-oh.png" /></li>
          <li><h1 href="">Yu-Gi-Oh-Api</h1></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style scoped>
header {
  background-color: white;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-list {
  list-style: none;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.nav-list img {
  width: 100px;
}

.nav-list h1 {
  text-decoration: none;
  color: black;
  font-size: 35px; /* Regola la dimensione del testo come preferisci */
}
</style>
