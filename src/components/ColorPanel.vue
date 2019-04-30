<template>
    <div>
        <Pixel color="blue" :current="color == 'blue' ? true : false"/>
        <Pixel color="lightblue" :current="color == 'lightblue' ? true : false"/>
        <Pixel color="darkblue" :current="color == 'darkblue' ? true : false"/>
        <Pixel color="white" :current="color == 'white' ? true : false"/>
    </div>
</template>

<<script>
import Pixel from './Pixel'

export default {
    name: 'ColorPanel',
    components: {
        Pixel
    },
    props: {
        color: String
    }
}
</script>