/* src/components/Fotos.vue */
<template>
  <div>
    <h2>Fotos</h2>
    <h2>Apartamento "X"</h2>
    <div id="entorno" class="galeria">
      <a href="Imagenes/11 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/11 APARTAMENTO X.webp" alt="Foto 1" /></a>
      <a href="Imagenes/12 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/12 APARTAMENTO X.webp" alt="Foto 2" /></a>
      <a href="Imagenes/13 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/13 APARTAMENTO X.webp" alt="Foto 3" /></a>
      <a href="Imagenes/14 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/14 APARTAMENTO X.webp" alt="Foto 4" /></a>
      <a href="Imagenes/15 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/15 APARTAMENTO X.webp" alt="Foto 5" /></a>
      <a href="Imagenes/16 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/16 APARTAMENTO X.webp" alt="Foto 6" /></a>
      <a href="Imagenes/17 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/17 APARTAMENTO X.webp" alt="Foto 7" /></a>
      <a href="Imagenes/18 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/18 APARTAMENTO X.webp" alt="Foto 8" /></a>
      <a href="Imagenes/19 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/19 APARTAMENTO X.webp" alt="Foto 9" /></a>
      <a href="Imagenes/20 APARTAMENTO X.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/20 APARTAMENTO X.webp" alt="Foto 10" /></a>
    </div>
    <h2>Apartamento "Y"</h2>
    <div class="galeria">
      <a href="Imagenes/21 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/21 APARTAMENTO Y.webp" alt="Foto 11" /></a>
      <a href="Imagenes/22 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/22 APARTAMENTO Y.webp" alt="Foto 12" /></a>
      <a href="Imagenes/23 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/23 APARTAMENTO Y.webp" alt="Foto 13" /></a>
      <a href="Imagenes/24 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/24 APARTAMENTO Y.webp" alt="Foto 14" /></a>
      <a href="Imagenes/25 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/25 APARTAMENTO Y.webp" alt="Foto 15" /></a>
      <a href="Imagenes/26 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/26 APARTAMENTO Y.webp" alt="Foto 16" /></a>
      <a href="Imagenes/27 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/27 APARTAMENTO Y.webp" alt="Foto 17" /></a>
      <a href="Imagenes/28 APARTAMENTO Y.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/28 APARTAMENTO Y.webp" alt="Foto 18" /></a>
    </div>
    <h2>Piscina y recreativos</h2>
    <div class="galeria">
      <a href="Imagenes/PISCINA.jpg" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/PISCINA.jpg" alt="Foto 19" /></a>
      <a href="Imagenes/PISCINA 2.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/PISCINA 2.webp" alt="Foto 20" /></a>
      <a href="Imagenes/PISTA DE TENIS.jpg" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/PISTA DE TENIS.jpg" alt="Foto 21" /></a>
      <a href="Imagenes/RECREATIVOS.webp" target="_blank" rel="noopener noreferrer"> <img src="Imagenes/RECREATIVOS.webp" alt="Foto 22" /></a>
    </div>
  </div>
</template>


<style scoped>
/* legacy .gallery (may be unused) */
.gallery {
  display: flex;
  gap: 10px;
  justify-content: center;
  flex-wrap: wrap;
}
.gallery img {
  max-width: 400px;
  border-radius: 10px;
  display: block;
}

/* Responsive square thumbnails for .galeria */
.galeria{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  padding: 20px;
}

.galeria a {
  display: block;
  /* Default: three columns (minus gap) but don't exceed 350px */
  flex: 0 1 calc(33.333% - 10px);
  max-width: 350px;
  /* keep thumbnails perfectly square */
  aspect-ratio: 1 / 1;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0px 4px 6px rgba(0,0,0,0.2);
}

.galeria img{
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

/* Tablets: two columns */
@media (max-width: 768px) {
  .galeria a {
    flex: 0 1 calc(50% - 10px);
  }
}

/* Mobile: one column (full width) */
@media (max-width: 480px) {
  .galeria a {
    flex: 0 1 calc(100% - 10px);
    max-width: none;
  }
}

</style>
