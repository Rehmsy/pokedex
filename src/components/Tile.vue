<template>
  <div class="tile"
    :style="{ background: pokemon.color_1}"
    @click="$emit('selected', pokemon)"
    >
      <img :src="pokemon.url_image">
      <p>{{ pokemon.pokemon.replace(/^\w/, c => c.toUpperCase()) }}</p>
  </div>
</template>

<script>

export default {
  data() {
    return {
      
    }
  },
  props: ['pokemon']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tile {
  width: 130px;
  height: 130px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 5px;
  padding: 5px;
  border-radius: 8px;
  opacity: 0.8;
  transition: all 1s ease;
}

p {
  text-align: center;
  font-size: 1em;
  margin-top: 5px;
}

.tile:hover {
  opacity: 1;
}

img {
  max-width: 80px;
  max-height: 80px;
}
</style>
