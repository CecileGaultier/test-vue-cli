<template>
  <div class="app">
    <button @click="$refs.dialog.visible=true">Open</button>

    <SimpleDialog ref="dialog"/>

  </div>
</template>

<script>

  import SimpleDialog from "@/SimpleDialog";

  export default {
  name: 'App',
  components: {
    SimpleDialog
  },
  data: function () {
    return{
      //plus de données
    }
  },
}
</script>

