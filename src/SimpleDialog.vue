<template>
    <div class="dialog-parent">
        <transition name="fade">
            <div class="dialog-backdrop" v-show="visible"></div>
        </transition>

        <transition name="zoom">
            <div class="dialog-window" v-show="visible">
                <header>
                    <h1>{{titre}}</h1>
                </header>
                <div class="main">
                    <slot/>
                </div>
                <footer>
                    <button @click="visible = false" v-if="show">Close</button>
                </footer>
            </div>
        </transition>


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

<style scoped>
    .dialog-window {
        position: relative;
        pointer-events: auto;
        transform: scale(2);
    }
    .dialog-parent {
        pointer-events: none;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .dialog-parent,
    .dialog-backdrop {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;

    }
    .dialog-backdrop {
        pointer-events: auto;
        background-color: rgba(255, 30, 80, 0.5);
    }

    .fade-enter-active{
        animation: fade 2s reverse;
    }

    .fade-leave-active{
        animation: fade 2s;
    }

    .zoom-enter-active{
        animation: zoom 2s ;

    }

    .zoom-leave-active{
        animation: zoom 2s reverse;
    }

    @keyframes fade{
        0% {
            opacity: 100%;
        }
        50% {
            opacity: 50%;
        }
        100% {
            opacity: 0;
        }
    }

    @keyframes zoom {
        0% {
            transform: scale(0);
        }
        50% {
            transform: scale(3);
        }
        100% {
            transform: scale(2);
        }

    }



</style>