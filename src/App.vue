<template>
<div>
    <li v-for="item in sampleArray">
        {{item}}
    </li>
    <li v-for="item in otherArray">
        {{item.id}} : {{item.name}}
    </li>
</div>
</template>

<script>
export default {
    setup() {
        return {
            sampleArray: ['a', 'b', 'c', 'd'],
            otherArray: [{
                    id: 0,
                    name: 'name0'
                },
                {
                    id: 1,
                    name: 'name1'
                },
                {
                    id: 2,
                    name: 'name2'
                },
                {
                    id: 3,
                    name: 'name3'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
