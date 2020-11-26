<template>
  <div class="app">
      <h1>Bonjour</h1>
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
      imageData:[]
    }
    },
      computed:{
        imageDataFiltree(){
            return [
                {
                    "src": "images/thumbnails/animals-1.jpeg",
                    "dataFullImg": "images/animals-1.jpeg",
                    "title": "gorille"
                },
                {
                    "src": "images/thumbnails/animals-2.jpeg",
                    "dataFullImg": "images/animals-2.jpeg",
                    "title": "biche"
                },
                {
                    "src": "images/thumbnails/animals-3.jpeg",
                    "dataFullImg": "images/animals-3.jpeg",
                    "title": "cochon"
                },
                {
                    "src": "images/thumbnails/animals-4.jpeg",
                    "dataFullImg": "images/animals-4.jpeg",
                    "title": "rhino"
                },
                {
                    "src": "images/thumbnails/animals-5.jpeg",
                    "dataFullImg": "images/animals-5.jpeg",
                    "title": "chat"
                },
                {
                    "src": "images/thumbnails/animals-6.jpeg",
                    "dataFullImg": "images/animals-6.jpeg",
                    "title": "chiot"
                },
                {
                    "src": "images/thumbnails/animals-7.jpeg",
                    "dataFullImg": "images/animals-7.jpeg",
                    "title": "tigre"
                },
                {
                    "src": "images/thumbnails/animals-8.jpeg",
                    "dataFullImg": "images/animals-8.jpeg",
                    "title": "girafe"
                },
                {
                    "src": "images/thumbnails/animals-9.jpeg",
                    "dataFullImg": "images/animals-9.jpeg",
                    "title": "chien"
                },
            this.imageData];
        }
      }
}
</script>

