<template>
    <div>
        <slot>
            <div class="parallax" :style="{ backgroundImage: `url(${backgroundUrl})` }"> 
                <h1 class="parallax-text" >
                    <label 
                        class="p-3" 
                        @mousemove="calcMousePos"
                        @mouseleave="isOnHover = false"
                    >Experience The Truth</label> 
                    </h1>
                <div v-if="isOnHover === true" class="hoverable-text" :style="{ top: top, left: left}" >
                    <h1>ASDASD</h1>
                </div>
            </div>
        </slot>
    </div>

    
    
</template>

<script>
import backgroundUrl from '../../assets/gt.jpg';

export default {
    name: 'FirstParallax',
    data() {
        return{
            backgroundUrl: backgroundUrl,
            isOnHover: false,
            top: 0,
            left: 0

        }
    },
    methods: {
        calcMousePos(event) {
            this.top = (event.pageY - 30) + 'px';
            this.left = event.pageX + 'px';
            this.isOnHover = true;
        }
    },

}
</script>

<style>
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
</style>