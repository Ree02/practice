<template>
    <!-- @inputで受け取った値をevenr引数で受け取ってgetInputValueメソッド発火-->
    <input type="text" @input="getInputValue">

</template>

<script>
export default {
    methods: {
        getInputValue($event) {
            this.$emit("input", $event.target.value);
        }
    }
}
</script>


<style>
.nuxt-logo {
  height: 180px;
}
</style>
