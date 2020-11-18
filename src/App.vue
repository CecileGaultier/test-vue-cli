<template>
  <div class="app">
      <h1>Bonjour</h1>
    <LightBox :initial-images-data="imageData" />


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
              "dataFullImg": "images/animals-1.jpeg"
          },
          {
              "src": "images/thumbnails/animals-2.jpeg",
              "dataFullImg": "images/animals-2.jpeg"
          },
          {
              "src": "images/thumbnails/animals-3.jpeg",
              "dataFullImg": "images/animals-3.jpeg"
          },
          {
              "src": "images/thumbnails/animals-4.jpeg",
              "dataFullImg": "images/animals-4.jpeg"
          },
          {
              "src": "images/thumbnails/animals-5.jpeg",
              "dataFullImg": "images/animals-5.jpeg"
          },
          {
              "src": "images/thumbnails/animals-6.jpeg",
              "dataFullImg": "images/animals-6.jpeg"
          },
          {
              "src": "images/thumbnails/animals-7.jpeg",
              "dataFullImg": "images/animals-7.jpeg"
          },
          {
              "src": "images/thumbnails/animals-8.jpeg",
              "dataFullImg": "images/animals-8.jpeg"
          },
          {
              "src": "images/thumbnails/animals-9.jpeg",
              "dataFullImg": "images/animals-9.jpeg"
          }
      ]

    }
  },
}
</script>

