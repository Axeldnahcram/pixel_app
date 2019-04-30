<template>
    <div @click="changeColor(color)" :class="['pixel', color, current ? 'current': '']"></div>
</template>

<script>
export default {
    name: "Pixel",
    props: {
        color: String,
        current: Boolean
    },
    methods: {
        changeColor: function(color){
            this.$root.$emit('updatecolor', color)
        }
    }
}
</script>

<style scoped>
.pixel {
    border: 1px solid lightgrey;
    width: 30px;
    height: 30px;
    box-sizing: border-box;
}
.white {
    background-color: white;
}
.lightblue {
    background-color: lightblue;
}
.blue {
    background-color: rgb(3, 169, 244);
}
.darkblue {
    background-color: darkblue;
}
.pixel.current {
    border: 4px solid yellow;
}
</style>
