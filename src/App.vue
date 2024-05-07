<template>
    <div>
        {{ count }}
    </div>
    <h1>Life Cycle Hooks</h1>
</template>

<script>
export default {
    data() {
        return {
            count: 0,
        }
    },
    beforeCreate() {
        console.log('beforeCreate', this.count);
    },

    created() {
        console.log('created', this.count);
        this.test();
      },
      
    beforeMount() {
      console.log('beforeMount', document.querySelector('h1'));
    },
    
    mounted() {
      console.log('mounted', document.querySelector('h1'));
    },

    methods: {
        test() {
            console.log('함수호출');
        }
    }
}
</script>

<style lang="scss" scoped>

</style>