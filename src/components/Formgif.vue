<template>
  <div>
    <div @submit.prevent="getNewCatGif()">
      <div>
        <label for="">Titulo</label>
        <input type="text" v-model="form.title" />
      </div>
      <div>
        <label for="">Titulo</label>
        <select required name="filtro" v-model="form.filter">
          <option value="" selected disabled></option>
          <option value="blur">Blur</option>
          <option value="mono">Mono</option>
          <option value="sepia">Sepia</option>
          <option value="negative">Negative</option>
          <option value="paint">Paint</option>
        </select>
      </div>
      <div>
        <label for="">Color</label>
        <select required name="color" v-model="form.color">
          <option value="" selected disabled></option>
          <option value="red">Rojo</option>
          <option value="blue">Azul</option>
          <option value="green">Verde</option>
          <option value="purple">Morado</option>
          <option value="orange">Naranja</option>
        </select>

        <span
          style="
            width: 15px;
            height: 15px;
            border-radius: 50%;
            display: inline-block;
          "
          :style="{ 'background-color': form.color }"
        ></span>
      </div>

      <label for="">Tamaño</label>
      <input
        type="number"
        name="tamaño"
        required
        step="100"
        min="100"
        max="900"
        v-model.number="form.size"
      />


       <button type="submit">Obtener gatito</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "gifform",
  
  props: {
    formGif: String,
  },

};
</script>

<style scoped>
</style>