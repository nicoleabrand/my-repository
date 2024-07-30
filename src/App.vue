<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <h1>Membros Hackathon</h1>
      <nav>
        <div class="btn">
                <RouterLink to="/Equipe">Equipe:</RouterLink>
        </div>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}

h1{
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  font-style: normal;
  font-size: 400%;
  text-align: left;
  padding: 2%;
  padding-bottom: 0px;
 
}

header{
  background-color: rgb(124, 124, 124);
  color: rgb(0, 0, 0);
}

nav{
  color: rgb(5, 0, 0);
  text-align: left;
  margin-top: 0%;
  padding-bottom: 3%;
  margin-left: 2%;
  padding-top: 1%;
}
a{
  color: rgb(122, 117, 117);
background: #e7e7e7;
border-radius: 3px;
}
</style>
