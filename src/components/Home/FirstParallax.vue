<template>
    <div>
        <slot>
            <div class="parallax" :style="{ backgroundImage: `url(${backgroundUrl})` }"> 
                
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
            backgroundUrl
        }
    }
}
</script>

<style>
    .parallax {
        -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
        filter: grayscale(100%);
        min-height: 400px;
        background-attachment: fixed;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
</style>