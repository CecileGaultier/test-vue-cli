<template>
    <div class="light-box">
        <transition-group name="list" tag="ul">
            <li v-for="{src, dataFullImg,title} in imageData" :key="src">
                <img :src="src" :title="title" @click="afficheImg(dataFullImg,title)" alt=""/></li>
        </transition-group>

        <SimpleDialog ref="dialog"
                      :titre="titre">
            <img :src="imageCourante" alt=""
                 width="400" height="200">

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
            titre: "",

        }
        },

        props: {
            imageData:{
                type: Array,
            }
        },

    methods:{
        afficheImg(url,titre){
            this.imageCourante = url;
            this.$refs.dialog.show();
            this.titre = titre
        }
    }
    }
</script>

<style scoped>

</style>