<template>
  <div class="destino-card">
    <h2 class="destino-titulo">{{ destino.titulo }}</h2>
    <p class="destino-descripcion">{{ destino.descripcion }}</p>
    <div class="destino-imagen-container">
      <img :src="destino.imagen" :alt="destino.titulo" class="destino-imagen">
    </div>
    <div class="precio">$ {{ destino.precio.toLocaleString("es-CO") }}</div>
    <button class="comprar-btn" @click="comprarDestino(destino)">Comprar</button>
  </div>
</template>

<script>
export default {
  name: 'DestinoCard',
  props: {
    destino: {
      type: Object,
      required: true,
      default: () => ({
        id: null,
        titulo: '',
        descripcion: '',
        imagen: '',
        precio: 0
      })
    }
  },
  methods: {
    comprarDestino(destino) {
      this.$emit('comprar-destino', destino);
    }
  }
};
</script>

<style scoped>
.destino-card {
  display: flex;
  flex-direction: column;
  border: 1px solid #ccc;
  padding: 15px;
  margin-bottom: 20px;
  border-radius: 8px;
  text-align: center;
}

.destino-titulo {
  margin-bottom: 5px; 
}

.destino-descripcion {
  margin-bottom: 10px; 
  font-size: 0.9em;
  color: #555;
}

.destino-imagen-container {
  max-height: 150px; 
  margin-bottom: 10px; 
  display: flex;
  justify-content: center; 
  align-items: center; 
}

.destino-imagen {
  max-width: 100%;
  max-height: 100%; 
  border-radius: 5px;
}

.precio {
  font-weight: bold;
  font-size: 1.2em;
  color: green;
  margin-bottom: 10px;
}

.comprar-btn {
  background-color: #28a745;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin-top: auto; 
}

.comprar-btn:hover {
  background-color: #1e7e34;
}
</style>