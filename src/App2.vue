<template>
<div>
    {{rawHtml}}
    {{rawHtml2}}
    <h1 v-html="rawHtml2"></h1>

    <h2 :class="{active:isActive}">클래스 바인딩</h2>
    <button @click="change">버튼</button>

    <h3 style="color: blue; font-size:24px">스타일 바인딩</h3>
    <h3 :style="{ color: '#888888', fontSize: '24px' }">스타일 바인딩</h3>
</div>
</template>

<script>
export default {
    data() {
        return {
            rawHtml: '텍스트',
            rawHtml2: '<span style="color: red">HTML</span>',
            isActive: false,
        }
    },
    methods: {
        change() {
            this.isActive = !this.isActive;
        }
    }
}
</script>

<style scoped>
h2.active {
    color: green;
}
</style>
