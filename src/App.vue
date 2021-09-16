 <template>
  <div>
    <h2>Gif cat app</h2>
    <p>aaddaa</p>
    <Viewgif/>
  </div>
</template>

<script>
import Viewgif from './components/Viewgif.vue'
// import HelloWorld from './components/HelloWorld.vue'
// import HelloWorld from './components/HelloWorld.vue'
// import HelloWorld from './components/HelloWorld.vue'
// import Gifform from "./Gifform.vue";
// import viewgif from "./Viewgif.vue";

export default {
  name: "App",
  components: {
    Viewgif
    // Formgif,
    //Viewgif
  },
  data: () => ({
    catUrl: "",
    form: {
      title: null,
      filter: null,
      color: null,
      size: null,
    },
  }),
  methods: {
    getNewCatGif() {
      this.gatitoUrl = `https://cataas.com/cat/gif/says/${this.formulario.titulo}?filter=${this.formulario.filtro}&color=${this.formulario.color}&width=${this.formulario.tamaño}&height=${this.formulario.tamaño}`;
    },
  },
};
</script>

<style scoped>
</style>
