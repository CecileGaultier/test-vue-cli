<template>
    <div class="light-box">
        <ul>
            <li v-for="{src, dataFullImg} in imageData" :key="src">
                <img :src="src" @click="afficheImg(dataFullImg)" alt=""/></li>
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
            imageData:[],
        }
    },
        created(){
            if (typeof this.initialImageData === 'string'){
                fetch(this.initialImageData)
                    .then(rep =>rep.json())
                    .then(json=>this.imageData =json);
            }
            else{
                this.imageData = this.initialImageData;
            }

        },

        props: {
            initialImageData:{
                type: [String,Array],
                default:"images-data.json",
            }
        },

    methods:{
        afficheImg(url){
            this.imageCourante = url;
            this.$refs.dialog.show();
        }
    }
    }
</script>

<style scoped>

</style>