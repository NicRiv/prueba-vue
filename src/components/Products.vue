<template>
  <div class="productos" v-for="item in productos" :key="item.id">
    <p>{{ item.nombre }}</p>

    <img :src="`/images/${item.producto}.jpg`" :alt="`Imagen del producto ${item.nombre}`" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      productos: [
        {
          nombre: 'microW200 Syn-L',
          producto: 'img1',
          numero: 1
        },
        {
          nombre: 'fastW700 Syn-L',
          producto: 'img2',
          numero: 2
        }
      ]
    }
  }
}
</script>

<style>
.productos {
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  justify-content: center;
  margin-top: 1rem;
  margin-bottom: 1rem;
  max-width: 17rem;
  padding: 0.4rem 0.3rem;
  border: 1px solid;
  border-radius: 7%;
  box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);
}

.productos p {
  font-size: large;
  margin-bottom: 0.5rem;
  font-weight: bold;
}

img {
  width: 250px;
}

@media (min-width: 1024px) {
  .productos {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 1rem;
    margin-bottom: 1rem;
    padding: 1rem 0.5rem 1rem 0.5rem;
    border: 1px solid;
    max-width: 20rem;
  }
}
</style>
