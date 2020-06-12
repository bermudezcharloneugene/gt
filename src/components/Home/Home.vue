<template>
    <div class="mt-5">
        <div class="container">
            <div v-scrollanimation> 
                <h1  class="text-center mt-3 text-style-1">
                    Fullstack Web Developer
                </h1>
                <!-- <img  :src="profileImage" alt="..." class="img-thumbnail rounded mx-auto d-block img-size"> -->
                <h5 class="text-center mt-3 text-style-1"  >
                    Hello, I'm Eugene Bermudez
                </h5>
            </div>
            <cards/>
        </div>
       <first-parallax />
        <about  />
    </div>
</template>

<script>

import profileImage from '../../assets/Eugene.jpg'
import divImage from '../../assets/gt.jpg'
import cards from './Cards';
import about from './About';
import FirstParallax from './FirstParallax'

export default {
    name: 'Home',
    components: {
        cards,
        firstParallax: FirstParallax,
        about
    },
    data() {
        return {
            profileImage: profileImage,
            divImage: divImage,
            showImage: false,
        }
    },
    methods: {
        showHeader() {
            this.showImage = true
        }
    },
    created() {
        window.addEventListener("load", this.showHeader);
    },
}
</script>

<style >
    @import url('https://fonts.googleapis.com/css2?family=Inconsolata&display=swap');


    .img-size {
        height: 150px;
        border-radius: 50%!important;
        object-position: center;
        object-fit: cover;
    }

    .image-background {
        height: 400px;
        width: 100%;
    }

    .text-style-1 {
        font-family: 'Inconsolata', monospace;
    }

    .before-enter {
        transform: translateX(-300px);
        opacity: 0;
        transition: all 2s ease-out;
    }

    .enter {
        transform: translateX(0px);
        opacity: 1;
    }
</style>