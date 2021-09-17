 <template>
  <div>
    <h2>Gif Cat App</h2>
    <!-- hijo que habla -->
    <Formgif @data-gif="getNewCatGif" />
    <!-- hijo que escucha -->
    <Viewgif :catUrl="catUrl" />
    <!-- funciona sin hijo <img :src="catUrl" alt=""> -->
  </div>
</template>

<script>
import Viewgif from "./components/Viewgif.vue";
import Formgif from "./components/Formgif.vue";

export default {
  name: "App",
  components: {
    Viewgif,
    Formgif,
  },
  data: () => ({
    catUrl: "",
  }),
  methods: {
    getNewCatGif(dataGif) {
      this.catUrl = `https://cataas.com/cat/gif/says/${dataGif.title}?filter=${dataGif.filter}&color=${dataGif.color}&width=${dataGif.size}&height=${dataGif.size}`;
      // console.log('datagif', dataGif);
      console.log("caturl", this.catUrl);
    },
  },
};
</script>

<style>
body {
  background-color: rgb(63, 219, 240);
  margin: 0;
  padding: 0;
}
h2 {
  text-align: center;
  color: white;
}
</style>
