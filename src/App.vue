<template>
  <div id="app">
    <header>
      <h1>Casa Rural María Luisa</h1>
      <a href="https://www.google.com/maps/dir//40.3690735,-5.750654/@40.3691104,-5.7504321,108m/data=!3m1!1e3!5m1!1e2?entry=ttu&g_ep=EgoyMDI1MDIxOS4xIKXMDSoASAFQAw%3D%3D" target="-blak" rel="noopener noreferrer" style="color:violet">Calle S.A.U.3,4 (Cruz Nueva, S/N), 37710 Candelario, Salamanca</a>
      <nav>
        <button @click="currentTab = 'informacion'">INFORMACIÓN</button>
        <button @click="currentTab = 'fotos'">FOTOS</button>
        <button @click="currentTab = 'entorno'">ENTORNO</button>
        <button @click="currentTab = 'quienesSomos'">QUIÉNES SOMOS</button>
      </nav>
    </header>

    <main>
      <InformacionRural v-if="currentTab === 'informacion'" />
      <GaleriaFotos v-if="currentTab === 'fotos'" />
      <EntornoCercano v-if="currentTab === 'entorno'" />
      <QuienesSomos v-if="currentTab === 'quienesSomos'" />
    </main>
  </div>
  <!-- Pie de página -->
   <footer class="footer">
     &copy; {{new Date ().getFullYear() }} Casas Rurales. Todos los derechos reservados
   </footer>
</template>

/* src/App.vue */
<script>
import { ref } from 'vue';
import InformacionRural from './components/InformacionRural.vue';
import GaleriaFotos from './components/GaleriaFotos.vue';
import EntornoCercano from './components/EntornoCercano.vue';
import QuienesSomos from './components/QuienesSomos.vue';
export default {
  components: { InformacionRural, GaleriaFotos, EntornoCercano, QuienesSomos },
  setup() {
    const currentTab = ref('informacion');
    return { currentTab };
  }
};

</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f8f8f8;
  text-align: center;
}

header {
  background-color: #007BFF;
  color: white;
  padding: 10px 0;
}

nav {
  /* horizontal nav that doesn't wrap; allows horizontal scroll on small screens */
  display: flex;
  gap: 10px;
  justify-content: center;
  flex-wrap: nowrap;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  padding: 8px 10px;
}

nav::-webkit-scrollbar { display: none; }
nav { scrollbar-width: none; }

nav button {
  flex: 0 0 auto;
  margin: 0 5px;
  padding: 10px 16px;
  background-color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

main {
  padding: 20px;
  background-color: white;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  margin: 20px auto;
  max-width: 800px;
}

</style>

<style scoped>
/* Estilo de pie de página */
.footer{
  text-align: center;
  padding: 10px 0;
  background-color: #0078d4;
  color: white;
  margin-top: 20px;
  border-radius: 0 0 10px 10px;
}
</style>