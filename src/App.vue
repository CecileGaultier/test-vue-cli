<template>
  <div class="app">
      <h1>Bonjour</h1>
      <button @click="filtreType='domestique'">domestique</button>
      <button @click="filtreType='sauvage'">sauvage</button>

      <LightBox :image-data="imageDataFiltree" />


  </div>
</template>

<script>

  import LightBox from "@/components/LightBox";

  export default {
  name: 'App',
  components: {LightBox},
  data: function () {
    return{
      imageData:[
          {
          "src": "images/thumbnails/animals-1.jpeg",
          "dataFullImg": "images/animals-1.jpeg",
          "title": "gorille",
              "type": "sauvage",
            },
          {
              "src": "images/thumbnails/animals-2.jpeg",
              "dataFullImg": "images/animals-2.jpeg",
              "title": "biche",
              "type": "sauvage",

          },
          {
              "src": "images/thumbnails/animals-3.jpeg",
              "dataFullImg": "images/animals-3.jpeg",
              "title": "cochon",
              "type": "domestique",
          },
          {
              "src": "images/thumbnails/animals-4.jpeg",
              "dataFullImg": "images/animals-4.jpeg",
              "title": "rhino",
              "type": "sauvage",
          },
          {
              "src": "images/thumbnails/animals-5.jpeg",
              "dataFullImg": "images/animals-5.jpeg",
              "title": "chat",
              "type": "domestique",
          },
          {
              "src": "images/thumbnails/animals-6.jpeg",
              "dataFullImg": "images/animals-6.jpeg",
              "title": "chiot",
              "type": "domestique",
          },
          {
              "src": "images/thumbnails/animals-7.jpeg",
              "dataFullImg": "images/animals-7.jpeg",
              "title": "tigre",
              "type": "sauvage",
          },
          {
              "src": "images/thumbnails/animals-8.jpeg",
              "dataFullImg": "images/animals-8.jpeg",
              "title": "girafe",
              "type": "sauvage",
          },
          {
              "src": "images/thumbnails/animals-9.jpeg",
              "dataFullImg": "images/animals-9.jpeg",
              "title": "chien",
              "type": "domestique",
          }],
        filtreType: "",
    }
    },
      computed:{
        imageDataFiltree(){
            return this.imageData.filter(({type})=>type===this.filtreType);
        }
      }
}
</script>

