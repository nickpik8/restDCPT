<template>
    <nav>
        <NavItem v-bind:list="nav.listItem"/>
    </nav>
</template>
<script>
import NavItem from '@/components/NavItem'
export default {
    name: 'Navigation',
    props: {
        nav: Object
    },
    components: {
        NavItem
    }
}
</script>

<style scoped>

</style>