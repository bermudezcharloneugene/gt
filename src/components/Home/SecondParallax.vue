<template>
    <div class="second-parallax" :style="{backgroundImage: `url(${backgroundUrl2})`}">

    </div>
</template>

<script>
import backgroundUrl2 from '../../assets/gt2.jpg';

export default {
    name: 'SecondParallax',
    data() {
        return {
            backgroundUrl2
        }
    }
}
</script>

<style scoped>
    .second-parallax {
            -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
            filter: grayscale(100%);
        min-height: 400px;
        background-attachment: fixed;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
</style>