<script setup>
import { RouterLink, RouterView } from "vue-router";
// import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
   

      <nav>
        <RouterLink :to="{ name: 'EventList'}">Events</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/test">Test</RouterLink>

      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  height: 5vh;
  min-height: 10vh;
    display: flex;
    align-items: flex-start;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 150%;
  font-size: 12px;
  text-align: center;
  margin-top: 0px;
}

nav a.router-link-exact-active {
 
  color: yellow;
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
    margin: 0 10rem 0 0;
  }

  header .wrapper {
    display: flex;
  
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
  h4 {
    font-size: 20px;
  }
}
</style>
