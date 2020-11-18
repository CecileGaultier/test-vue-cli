<template>
  <div class="app">
      <h1>Bonjour</h1>
    <light-box/>


  </div>
</template>

<script>

  import LightBox from "@/components/LightBox";

  export default {
  name: 'App',
  components: {
    LightBox
  },
  data: function () {
    return{
      //plus de données
    }
  },
}
</script>

