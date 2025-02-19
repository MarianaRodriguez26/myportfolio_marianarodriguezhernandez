<template>

<header class="hero">
  <div class="container">
      <h2>Bienvenido a mi Portafolio</h2>
      <h3>Desarrollador Web & Diseñador Gráfico</h3>
    <div class="Cont2">
        <img src="../assets/DIBUJOS MAR/IMG-20241104-WA0020.jpg" alt="Foto de perfil" class="profile-img">
      <div class="about">
            <h3>Sobre mí</h3>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iusto dolorem nihil fuga ipsam perferendis, quisquam possimus labore accusamus commodi recusandae aliquid doloremque pariatur eum dignissimos maxime quasi vero cupiditate eos.
          </p>
          <br>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate, praesentium at. A placeat nisi nobis accusantium et reprehenderit dicta iste quo ex soluta! Eligendi non ipsam quisquam eum eos? Laudantium?</p>
      </div>
    </div>
  </div>
</header>

<section class="gallery">
  <div class="container">
      <h2>Galería de Proyectos</h2>
      <div class="gallery-grid">
        <div class="gallery-item">
            <img src="../assets/Book Store Concept 📚.jpg" alt="Proyecto 1">
            <p class="">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus nisi accusantium minima reiciendis? Modi repellat, eaque labore magnam autem neque quibusdam quos blanditiis animi explicabo nihil nulla alias nemo et?</p>
        </div>
        <div class="gallery-item">
            <img src="../assets/Book Store Concept 📚.jpg" alt="Proyecto 2">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste quam minus eum optio deleniti cumque ratione explicabo ipsa unde ea magni molestias distinctio obcaecati, alias nihil architecto, inventore non soluta!</p>
        </div>
        <div class="gallery-item">
            <img src="../assets/Book Store Concept 📚.jpg" alt="Proyecto 3">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Maiores nemo magni cum unde quod, qui et cupiditate vero. Voluptatibus deleniti quas non vero, commodi earum? Qui odit ut obcaecati aliquam!</p>
        </div>
        <div class="gallery-item">
            <img src="../assets/Book Store Concept 📚.jpg" alt="Proyecto 4">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci at velit nulla aliquam dicta perspiciatis sapiente atque. Vitae quia nesciunt, iure pariatur nulla officiis ex nobis illum deleniti maxime eos?</p>
        </div>
        <div class="gallery-item">
            <img src="../assets/Book Store Concept 📚.jpg" alt="Proyecto 5">
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Enim modi velit ullam tenetur, eos corrupti placeat nobis quisquam iure laudantium ab exercitationem voluptate cum iste corporis inventore laboriosam a voluptates.</p>
        </div>
        <div class="gallery-item">
            <img src="../assets/Book Store Concept 📚.jpg" alt="Proyecto 6">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam saepe quae recusandae similique optio voluptatum ullam, harum assumenda consequatur sunt, cum officiis asperiores earum. Quae distinctio nemo consequatur sint enim?</p>
        </div>
      </div>
  </div>
</section>

<!-- Sección de Contacto -->
<section class="contact">
  <div class="container">
      <h2>Contacto</h2>
      <form>
          <input type="text" placeholder="Nombre">
          <input type="email" placeholder="Email">
          <textarea placeholder="Mensaje"></textarea>
          <button type="submit">Enviar Mensaje</button>
      </form>
  </div>
</section>
</template>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

*{
  font-family: "Roboto", serif;
}


/* Estilos generales */
p {
  text-align: justify;
  margin: 0; /* Eliminar márgenes por defecto del párrafo */
}

h3 {
  color: #a15b9d;
}

h2 {
  color: #570082;
}

.container {
  width: 90%;
  margin: auto;
  padding: 0;
  box-sizing: border-box;
}

.Cont2 {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 20px;
  max-width: 800px;
  margin: 20px auto;
  text-align: justify;
  margin-top: 40px;
}

.hero {
  text-align: center;
  padding: 50px 0;
  background: #fff;
}

.hero h2 {
  font-size: 2em;
}

.hero .profile-img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-top: 20px;
}

.about {
  margin-top: 20px;
  margin-right: 20px;
  margin-left: 20px;
}

.gallery {
  padding: 40px 0;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 columnas en computadoras */
  gap: 20px;
  max-width: 100%;
  justify-content: center;
  align-items: stretch; /* Asegura que todos los items tengan la misma altura */
}

.gallery-item {
  display: flex;
  flex-direction: column;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  background-color: #f9f9f9;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.gallery-item img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  margin-bottom: 15px; /* Espacio entre la imagen y el texto */
}

.gallery-item p {
  flex-grow: 1; /* Hace que el texto ocupe el espacio restante */
  overflow: hidden; /* Evita que el texto se desborde */
  text-overflow: ellipsis; /* Añade puntos suspensivos si el texto es muy largo */
}

.contact {
  text-align: center;
  padding: 40px 0;
  background: #fff;
}

.contact form {
  display: flex;
  flex-direction: column;
  align-items: center; /* Centrar elementos horizontalmente */
  width: 70%;
  margin: auto;
}

.contact input, .contact textarea {
  padding: 10px;
  margin: 10px 0;
  width: 70%; /* Ancho del 70% del contenedor del formulario */
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 16px;
  box-sizing: border-box;
}

.contact textarea {
  height: 150px; /* Altura fija para el textarea */
  resize: none; /* Evitar que el usuario cambie el tamaño */
}

.contact button {
  background: #ccadbc;
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
  border-radius: 5px;
  width: 70%; /* Ancho del 70% del contenedor del formulario */
  transition: background-color 0.3s ease; /* Transición suave para el hover y active */
}

.contact button:hover {
  background: #b89ca9; /* Color más oscuro al pasar el mouse */
}

.contact button:active {
  background: #a58b96; /* Color aún más oscuro al hacer clic */
}

/* Media Queries para responsividad */
@media (max-width: 1024px) {
  .gallery-grid {
    grid-template-columns: repeat(2, 1fr); /* 2 columnas en tablets */
  }
}

@media (max-width: 768px) {
  .Cont2 {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .hero .profile-img {
    width: 120px;
    height: 120px;
  }

  .gallery-grid {
    grid-template-columns: repeat(2, 1fr); /* 2 columnas en tablets pequeñas */
  }
}

@media (max-width: 480px) {
  .hero h2 {
    font-size: 1.5em;
  }

  .hero h3 {
    font-size: 1.2em;
  }

  .gallery-grid {
    grid-template-columns: 1fr; /* 1 columna en móviles */
  }

  .gallery-item {
    width: 100%;
  }
}

/* Media Queries para responsividad */
@media (max-width: 768px) {
  .contact form {
    width: 90%; /* Aumentar el ancho del formulario en dispositivos pequeños */
  }

  .contact input, .contact textarea, .contact button {
    width: 100%; /* Ocupar todo el ancho disponible en dispositivos pequeños */
  }
}
</style>