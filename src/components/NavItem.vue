<template>
    <div>
        <div  v-for="item in list" :key="item.id">
            {{ item.title }}
        </div>
    </div>
</template>
<script>
export default {
    name: 'NavItem',
    props: {
        list : Array
    }
}
</script>
<style scoped>

</style>