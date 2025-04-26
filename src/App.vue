<template>
  <div id="app">
    <nav class="top-full-width-nav-horizontal">
      <router-link to="/tours">Tours</router-link>
      <router-link to="/sobre-nosotros">Sobre Nosotros</router-link>
      <router-link to="/contacto">Contacto</router-link>
      <router-link to="/destinos-populares">Destinos Populares</router-link>
      <router-link to="/actividades">Actividades</router-link>
      <router-link to="/galeria">Galería</router-link>
    </nav>
    <main>
      <router-view />
    </main>
  </div>
</template>

<style>
body {
  margin: 0; 
  padding: 0; 
}

#app {
  font-family: 'Arial', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333333;
  position: relative; 
  width: 100%; 
}

nav.top-full-width-nav-horizontal {
  background-color: #343a40; 
  color: #ffffff;
  padding: 15px 20px; 
  position: fixed; 
  top: 0;
  left: 0;
  width: 100%; 
  z-index: 10; 
  display: flex; 
  align-items: center; 
  justify-content: flex-start; 
}

nav.top-full-width-nav-horizontal a {
  font-weight: bold;
  color: #ffffff;
  margin-right: 15px; 
  text-decoration: none;
  transition: color 0.3s;
}

nav.top-full-width-nav-horizontal a:last-child {
  margin-right: 0; 
}

nav.top-full-width-nav-horizontal a:hover {
  color: #adb5bd; 
}

main {
  padding: 20px;
  margin-top: 60px; 
  width: 100%; 
}
nav.top-full-width-nav-horizontal {
  display:flex;
  justify-content: space-evenly;
  align-items: center
}
</style>