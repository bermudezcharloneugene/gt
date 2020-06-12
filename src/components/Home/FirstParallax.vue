<template>
    <div class="mt-5">
        <slot >
            <div class="parallax" :style="{ backgroundImage: `url(${backgroundUrl})` }"> 
                <h1 class="parallax-text" >
                    <label 
                        class="p-3" 
                    >Experience The Truth</label> 
                </h1>
            </div>
        </slot>
    </div>
</template>

<script>
import backgroundUrl from '../../assets/gt.jpg';

export default {
    name: 'FirstParallax',
    props: ['checkImage'],
    data() {
        return{
            backgroundUrl: backgroundUrl,
        }
    },


}
</script>

<style scoped>
    .parallax {
        -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
        filter: grayscale(100%);
        min-height: calc(800px - 10rem);
        background-attachment: fixed;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
    .parallax-text {
        position: absolute;
        left: 40%;
        top: 40%;
        background: #000;
        color: white;

    }
    .hoverable-text {
        position: absolute;

        background: rgb(170, 168, 168);
        color: white;
        padding: 40px 50px 40px 50px;

    }

    .before-enter {
        opacity: 0!important;
        transition: opacity 1s !important;
    }

    .enter {
        opacity: 1;
        /* transition: opacity 1s; */
    }
</style>