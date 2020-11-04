<template>
    <div id="app">
        <div class="dialog-window" v-show="visible">
            <header>
                <h1>{{titre}}</h1>
            </header>
            <div class="main">
                Contenu
            </div>
            <footer>
                <button @click="visible=false">Close</button>
            </footer>
        </div>

    </div>
</template>
<script>
    export default {
        name: 'SimpleDialog',
        props: {
            initialVisible:{
                type:Boolean,
                default:false,
            },
            titre:{
               type: String,
                default: "Le titre par défaut",
            }
        },
        data:function () {
            return{
                visible:this.initialVisible,
            }
        },
        methods:{
            show(){
                this.visible=true;
            }
        }
    }
</script>
