<template>
    <div>
        Practice
        <PracticeInput v-model="getText"/>
        <PracticeButton @onClick="showText"/>
        <p v-if="show">{{ getText }}</p>
    </div>
</template>

<script>
import PracticeInput from '../components/PracticeInput.vue'
import PracticeButton from '../components/PracticeButton.vue'
export default {
    // 変数の定義
    data() {
        return {
            show: false,
            getText: ''
        }
    },
    component: {
        PracticeInput,
        PracticeButton 
    },
    methods: {
        showText(isShow) {
            this.show = isShow;
            // console.log("親: " + this.show);
            // console.log("入力された値: " + this.text);
        }
    }
}
</script>