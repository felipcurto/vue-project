<template>
  <div id="app">
    <header>
      <h1>Los Países Más Bonitos del Mundo</h1>
      <p>Explora algunos de los destinos más hermosos que nuestro planeta tiene para ofrecer.</p>
    </header>
    <main class="content">
      <div class="country-card" v-for="country in countries" :key="country.name">
        <img :src="country.image" :alt="country.name" />
        <h2>{{ country.name }}</h2>
        <p>{{ country.description }}</p>
      </div>
    </main>
    <footer>
      <p>© 2024 Los Países Más Bonitos del Mundo</p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      countries: [
        {
          name: 'Suiza',
          description: 'Montañas, lagos y paisajes impresionantes.',
          image: 'https://cdn0.bodas.net/article/8191/3_2/960/jpg/101918-shutterstock-2292901079.jpeg',
        },
        {
          name: 'Nueva Zelanda',
          description: 'Escenarios naturales y aventuras al aire libre.',
          image: 'https://viajes.nationalgeographic.com.es/medio/2019/03/19/milford-stones-clean_37e89155_800x800.jpg',
        },
        {
          name: 'Japón',
          description: 'Tradición y modernidad en armonía.',
          image: 'https://humanidades.com/wp-content/uploads/2017/07/japon-7-e1571188430646.jpg',
        },
        {
          name: 'Italia',
          description: 'Arte, historia y gastronomía.',
          image: 'https://fundacionio.com/wp-content/uploads/2020/10/Italia.png',
        },
        {
          name: 'Islandia',
          description: 'Paisajes volcánicos y auroras boreales.',
          image: 'https://www.civitatis.com/blog/wp-content/uploads/2020/02/que-ver-islandia.jpg',
        },
        {
          name: 'Canadá',
          description: 'Naturaleza salvaje y ciudades vibrantes.',
          image: 'https://media.iatiseguros.com/wp-content/uploads/2021/12/07174931/requisitos-viajar-canada-documentos-4.jpg',
        },
        {
          name: 'Australia',
          description: 'Playas impresionantes y vida salvaje única.',
          image: 'https://www.intermundial.es/blog/wp-content/uploads/2022/03/mejores-ciudades-de-australia.jpg',
        },
        {
          name: 'Noruega',
          description: 'Fiordos espectaculares y paisajes nevados.',
          image: 'https://www.noruegatours.com/wp-content/uploads/2021/12/noruega-en-febrero.png',
        }
      ]
    }
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  background-color: #fff; /* Fondo blanco */
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

header {
  background: #42b983;
  color: white;
  padding: 20px;
  text-align: center;
}

header h1 {
  margin: 0;
}

header p {
  margin: 10px 0 0;
}

.content {
  flex: 1;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 20px;
}

.country-card {
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  margin: 20px;
  max-width: 300px;
  text-align: left;
  overflow: hidden;
  transition: transform 0.3s;
}

.country-card:hover {
  transform: scale(1.05);
}

.country-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.country-card h2 {
  font-size: 1.5em;
  margin: 10px;
  color: #42b983;
}

.country-card p {
  font-size: 1em;
  color: #666;
  margin: 10px;
}

footer {
  background: #42b983;
  color: white;
  text-align: center;
  padding: 20px;
}
</style>

