<template>
    <div class="header-section ">
        <slot>
            <h1 class="header-text text-center p-5">Gene&Truth</h1>

        </slot>
    </div>
    
        
    
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style scoped>
    .header-section {
        background-color: black;
        min-height: 150px;
    }

    .header-text {
        color: rgb(255, 255, 255)
    }
</style>