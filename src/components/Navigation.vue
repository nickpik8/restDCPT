<template>
    <nav>
        <ul>
            <NavItem   
            v-for="item in nav.listItem" :key="item.id"
            v-bind:item="item"
            />
        </ul>
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
    nav{
        border-bottom: 1px solid #888;
        margin-top: 2rem;
    }
    ul{
        display: flex;
        flex-direction: column;
        list-style: none;
        justify-content: flex-end;
    }
    @media (min-width: 768px){
        ul{
            flex-direction: row;
        }
    }
</style>