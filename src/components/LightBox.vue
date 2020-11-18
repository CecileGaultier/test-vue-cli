<template>
    <div class="light-box">
        <ul>
            <li><img src="images/thumbnails/animals-2.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-2.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-1.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-1.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-3.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-3.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-4.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-4.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-5.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-5.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-6.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-6.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-7.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-7.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-8.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-8.jpeg'" alt=""/></li>
            <li><img src="images/thumbnails/animals-9.jpeg" @click="$refs.dialog.show(); imageCourante='images/animals-9.jpeg'" alt=""/></li>
        </ul>

        <SimpleDialog ref="dialog"
                      titre="Le titre de cette instance">
            <img :src="imageCourante" alt=""
                 width="400" height="200">
            <!-- On met la taille pour ne pas avoir à écrire
                  un code qui attend le chargement de l'image -->
        </SimpleDialog>

    </div>
</template>

<script>

    import SimpleDialog from "@/SimpleDialog";


    export default {
        name: "LightBox",
        components: {SimpleDialog},

    data: function () {
        return{
            imageCourante: "",
        }
    }
    }
</script>

<style scoped>

</style>