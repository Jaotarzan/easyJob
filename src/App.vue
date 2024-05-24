<script setup>
import { RouterView, RouterLink } from 'vue-router'
</script>

<template>
  <header>
    <div class="parte-1-header">
      <div id="logo container">
        <img src="../img/logo.png" alt="logo" id="logo" />
      </div>
      <div id="searchbar-container">
        <form class="d-flex" role="search" id="barra_pesquisa">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" />
          <button class="btn btn-outline-success" type="submit" id="btn-pesquisa">Search</button>
        </form>
      </div>
    </div>
    <nav>
      <RouterLink to="/" class="nav-btns">Home</RouterLink>
      <RouterLink to="/about" class="nav-btns">Perfil</RouterLink>
      <RouterLink to="/about" class="nav-btns">Trabalhos</RouterLink>
      <RouterLink to="/about" class="nav-btns">freelancers</RouterLink>
    </nav>
  </header>
  <main>
    <RouterView />
  </main>
  <footer>
    <p>Todos os direitos reservados ©EasyJob - 2024</p>
  </footer>
</template>

<style scoped>
* {
  border: none;
  padding: 0;
  margin: none;
  font-family: 'Roboto', sans-serif;
}

header {
  width: 100%;
  height: 15vh;
  background-color: rgb(29, 68, 141);
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.parte-1-header {
  display: flex;
  flex-direction: row;
  align-items: center;
}

#searchbar-container {
  width: 100%;
  display: flex;
  justify-content: center;
}

#btn-pesquisa {
  border: 1px solid rgb(10, 128, 10);
  width: 6vw;
}

#btn-pesquisa:hover {
  background-color: rgb(10, 128, 10);
}

#logo {
  max-height: 13vh;
  margin-top: 1vh;
}

#barra_pesquisa {
  width: 80%;
  height: 6vh;
}

header > nav {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.nav-btns {
  display: flex;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  color: white;
  height: 100%;
  font-size: larger;
  width: 25%;
}

.nav-btns:hover {
  background-color: rgb(7, 7, 77);
  transition: 0.5s;
}

footer {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 20vh;
  background-color: rgb(29, 68, 141);
}

footer > p {
  color: white;
}
</style>
