<template>
<nav class="navbar">
  <div class="container">
      <h1>Portfolio</h1>
      <button class="hamburger" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </button>
      <!-- Menú de navegación -->
      <ul class="nav-links" :class="{ 'active': isMenuOpen }">
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Gallery</a></li>
          <li><a href="#">Contact</a></li>
      </ul>
  </div>
</nav>

<main>
  <Home></Home>
</main>

<!-- Pie de Página -->
<footer class="footer">
    <div class="container1">
      <!-- Sección About Us -->
      <div class="footer-section">
        <h3>About us</h3>
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Distinctio doloremque pomo molestios temporibus omnis,
          aliquid dignissimos corrupti loborum q, vulputatibus lusio doloree enim lis nulla non fugo tempore eugenobili
          temporer similisper?
        </p>
      </div>

      <!-- Sección Quick Links -->
      <div class="footer-section">
        <h3>Quick Links</h3>
        <ul class="quick-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">About me</a></li>
          <li><a href="#">Gallery</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>

      <!-- Sección Contact -->
      <div class="footer-section">
        <h3>Contact</h3>
        <ul class="contact-info">
          <li>Email: info@youtafia.com</li>
          <li>Phone: (984) 285 7417</li>
          <li>Adress: Playa del Carmen, MX</li>
        </ul>
      </div>
    </div>

    <!-- Derechos de autor -->
    <div class="footer-bottom">
      <p>© 2026. By Mariana Rodríguez Hernández. All rights reserved.</p>
    </div>
  </footer>

</template>

<script>
import Home from './components/Home.vue';

export default {
  name: 'App',
  components: {
    Home,
  },
  data() {
    return {
      isMenuOpen: false, // Estado para controlar el menú desplegable
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen; // Alternar el estado del menú
    },
  },
};
</script>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

#app {
  font-family: "Roboto", serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #570082;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

h1 {
  color: #570082;
}

.navbar {
  background: #cca9db;
  color: #570082;
  padding: 20px 0;
  position: relative;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.container2 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 20px;
  margin: 0;
  padding: 0;
}

.nav-links li {
  display: inline;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  font-size: 1.1em;
}

/* Estilos para el botón de hamburguesa */
.hamburger {
  display: none; /* Ocultar en pantallas grandes */
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
}

.hamburger span {
  width: 25px;
  height: 3px;
  background: #fff;
  transition: all 0.3s ease;
}

/* Estilos para el menú en móviles */
@media (max-width: 768px) {
  .hamburger {
    display: flex; /* Mostrar en pantallas pequeñas */
  }

  
  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: #cca9db;
    flex-direction: column;
    align-items: center;
    gap: 0;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
  }

  .nav-links.active {
    max-height: 300px; /* Altura máxima para mostrar el menú */
  }

  .nav-links li {
    width: 100%;
    text-align: center;
    padding: 10px 0;
  }

  .nav-links a {
    font-size: 1.2em;
  }
}

/* Footer */
.footer {
  background-color: #a15b9d; /* Color de fondo oscuro */
  color: #fff; /* Color del texto */
  padding: 40px 0;
  font-family: "Roboto", serif;

}

.container1 {
  width: 90%;
  max-width: 1300px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap; /* Permite que las secciones se ajusten en pantallas pequeñas */
  gap: 20px;
  justify-content: space-between;
}

/* Estilos para cada sección del footer */
.footer-section {
  flex: 1; /* Cada sección ocupa el mismo espacio */
  min-width: 200px; /* Ancho mínimo para evitar que se compriman demasiado */
  margin-bottom: 20px;
}

.footer-section h3 {
  font-size: 1.5em;
  margin-bottom: 15px;
  color: #570082; /* Color del título */
}

.footer-section p {
  font-size: 0.9em;
  line-height: 1.6;
  color: #fff; /* Color del texto secundario */
}

/* Estilos para la lista de Quick Links */
.quick-links {
  list-style: none;
  padding: 0;
}

.quick-links li {
  margin-bottom: 10px;
}

.quick-links a {
  color: #fff;
  text-decoration: none;
  font-size: 0.9em;
  transition: color 0.3s ease;
}

.quick-links a:hover {
  color: #570082; /* Cambia el color al pasar el mouse */
}

/* Estilos para la sección de Contact */
.contact-info {
  list-style: none;
  padding: 0;
}

.contact-info li {
  margin-bottom: 10px;
  font-size: 0.9em;
  color: #fff; /* Color del texto secundario */
}

/* Estilos para el pie de página inferior */
.footer-bottom {
  text-align: center;
  padding: 20px 0;
  background-color: #cca9db; /* Color de fondo más oscuro */
  margin-top: 40px;
}

.footer-bottom p {
  margin: 0;
  font-size: 0.9em;
  color: #570082; /* Color del texto secundario */
}

/* Media Queries para responsividad */
@media (max-width: 768px) {
  .container {
    flex-direction: column; /* Cambia a una columna en pantallas pequeñas */
    align-items: center;
    text-align: center;
  }

  .footer-section {
    min-width: 100%; /* Ocupa todo el ancho en móviles */
  }

  .quick-links,
  .contact-info {
    text-align: center;
  }
}
</style>
