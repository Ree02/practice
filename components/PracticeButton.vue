<template>
    <!-- @inputで受け取った値をevenr引数で受け取ってgetInputValueメソッド発火-->
    <button @click="onClick">表示</button>
</template>

<script>
export default {
    // 変数の定義
    data() {
        return {
            isShow: false,
        }
    },
    methods: {
        onClick() {
          this.isShow = !this.isShow
          this.$emit("onClick", this.isShow);
        }
    }
}
</script>
