<template>
  <header class="header">
    <div class="logo">
      <img src="@/assets/images/logo.png" alt="TruckMe Logo" />
    </div>
    <nav class="nav-menu">
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">Sobre</router-link></li>
        <li><router-link to="/services">Serviços</router-link></li>
        <li><router-link to="/contact">Contato</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  background-color: #333;
  color: white;
}

.logo img {
  width: 120px;
}

.nav-menu ul {
  list-style-type: none;
  padding: 0;
  display: flex;
}

.nav-menu li {
  margin-right: 20px;
}

.nav-menu a {
  color: white;
  text-decoration: none;
  font-size: 18px;
}

@media screen and (max-width: 768px) {
  .header {
    flex-direction: column;
    align-items: flex-start;
    padding: 10px;
  }

  .nav-menu ul {
    margin-top: 10px;
  }

  .nav-menu li {
    margin-right: 0;
    margin-bottom: 10px;
  }
}
</style>
