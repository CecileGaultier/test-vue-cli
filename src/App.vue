<template>
  <SimpleDialog :visible="visible"/>
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
      visible:false,
    }
  },
}
</script>

