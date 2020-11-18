<template>
    <div class="light-box">
        <button @click="$refs.dialog.show()">Open</button>

        <SimpleDialog ref="dialog"
                      initial-visible titre="Le titre de cette instance">
            Contenu s'affiche dans ...
        </SimpleDialog>
    </div>
</template>

<script>

    import SimpleDialog from "@/SimpleDialog";


    export default {
        name: "LightBox",
        components: {SimpleDialog},
    }
</script>

<style scoped>

</style>