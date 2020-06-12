<template>
    <div v-scrollanimation id="about" class="mt-5 container">
        <h1>About Me</h1>
        <hr>
        <p>
          I'm a fullstack web developer with a degree in Information Technology. PHP is my first language then I  
        </p>
    </div>
</template>
<script>
export default {
    name: "about"
}
</script>
<style scoped>
    


    .before-enter {
        transform: translateX(100px);
        opacity: 0;
        transition: all 1s ease-out;
    }   
    .enter {
                opacity: 1;
        transform: translateX(0px);

        
    } 

</style>