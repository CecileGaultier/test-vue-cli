<template>
  <div class="app">
      <h1>Bonjour</h1>
      <button @click="filtreType=null">tous</button>
      <button v-for="type of listeFiltresType" :key="type" @click="filtreType=type">{{type}}</button>
      <h3>Je veux trier :</h3>
      <button v-for="tris of listeNomTris" :key="tris" @click="filtreNomTri=tris">{{tris}}</button>

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
              "tris": {
                  "taille": 1.4,
                  "poids": 80,
                  "age": 6
              }
            },
          {
              "src": "images/thumbnails/animals-2.jpeg",
              "dataFullImg": "images/animals-2.jpeg",
              "title": "biche",
              "type": "sauvage",
              "tris": {
                  "taille": 1.4,
                  "poids": 10,
                  "age": 1
              }

          },
          {
              "src": "images/thumbnails/animals-3.jpeg",
              "dataFullImg": "images/animals-3.jpeg",
              "title": "cochon",
              "type": "domestique",
              "tris": {
                  "taille": 1,
                  "poids": 30,
                  "age": 7
              }
          },
          {
              "src": "images/thumbnails/animals-4.jpeg",
              "dataFullImg": "images/animals-4.jpeg",
              "title": "rhino",
              "type": "sauvage",
              "tris": {
                  "taille": 1,
                  "poids": 80,
                  "age": 8
              }
          },
          {
              "src": "images/thumbnails/animals-5.jpeg",
              "dataFullImg": "images/animals-5.jpeg",
              "title": "chat",
              "type": "domestique canapé",
              "tris": {
                  "taille": 0.4,
                  "poids": 10,
                  "age": 1
              }
          },
          {
              "src": "images/thumbnails/animals-6.jpeg",
              "dataFullImg": "images/animals-6.jpeg",
              "title": "chiot",
              "type": "domestique",
              "tris": {
                  "taille": 0.4,
                  "poids": 10,
                  "age": 1
              }
          },
          {
              "src": "images/thumbnails/animals-7.jpeg",
              "dataFullImg": "images/animals-7.jpeg",
              "title": "tigre",
              "type": "sauvage",
              "tris": {
                  "taille": 1,
                  "poids": 30,
                  "age": 7
              }
          },
          {
              "src": "images/thumbnails/animals-8.jpeg",
              "dataFullImg": "images/animals-8.jpeg",
              "title": "girafe",
              "type": "sauvage",
              "tris": {
                  "taille": 5.4,
                  "poids": 30,
                  "age": 7
              }
          },
          {
              "src": "images/thumbnails/animals-9.jpeg",
              "dataFullImg": "images/animals-9.jpeg",
              "title": "chien",
              "type": "domestique",
              "tris": {
                  "taille": 0.4,
                  "poids": 10,
                  "age": 8
              }
          }],
        filtreType: null,
        filtreNomTri : null,
    }
    },
      computed:{
          imageDataFiltree(){
            if (this.filtreType){
                return this.imageData.filter(({type})=>type===this.filtreType);
            } else {
                return this.imageData;
            }
        },
          listeFiltresType(){
            return new Set(this.imageData.map(o=>o.type))
          },
          listeNomTris() {
              const imageDatum = this.imageData[0];
              return imageDatum ? Object.keys(imageDatum.tris) : [];
          }
      }
}
</script>

