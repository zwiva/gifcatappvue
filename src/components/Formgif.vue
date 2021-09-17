<template>
  <div class="form">
    <form @submit.prevent="getCatObject()">
      <div>
        <label for="">Titulo </label>
        <input type="text" v-model="formgif.title" />
      </div>
      <div>
        <label for="">Filtro </label>
        <select required name="filtro" v-model="formgif.filter">
          <option value="" selected disabled></option>
          <option value="blur">Blur</option>
          <option value="mono">Mono</option>
          <option value="sepia">Sepia</option>
          <option value="negative">Negative</option>
          <option value="paint">Paint</option>
        </select>
      </div>
      <div>
        <label for="">Color </label>
        <select required name="color" v-model="formgif.color">
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
          :style="{ 'background-color': formgif.color }"
        >
        </span>
      </div>
      <div>
        <label for="">Tamaño </label>
        <input
          type="number"
          name="tamaño"
          required
          step="100"
          min="100"
          max="900"
          v-model.number="formgif.size"
        />
      </div>

      <button class="btn" type="submit">Obtener gatito 😺</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Formgif",
  data: () => ({
    formgif: {
      title: null,
      filter: null,
      color: null,
      size: null,
    },
  }),
  methods: {
    getCatObject() {
      console.log("title", this.formgif.title);
      console.log("filter", this.formgif.filter);
      console.log("color", this.formgif.color);
      console.log("size", this.formgif.size);
      this.$emit("data-gif", this.formgif);
    },
  },
};
</script>

<style scoped>
.form {
  padding: 1em;
  background-color: rgb(255, 130, 199);
  display: block;
  margin: 0 auto;
}
form div {
  margin: 1em;
}
.btn {
  display: block;
  margin: 0 auto;
}
</style>