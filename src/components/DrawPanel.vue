<template>
    <div class="drawpanel">
        <Pixel v-for="n in 30*30" color="blue"/>
    </div>
</template>

<script>
import Pixel from './Pixel'

export default {
    name: 'DrawPanel',
    components: {
        Pixel
    }
}
</script>

<style scoped>
.drawpanel {
    display: flex;
    flex-wrap: wrap;
    max-width: 900px
}
</style>