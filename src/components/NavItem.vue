<template>
    <li class="m-2">
        <router-link to="item.href">
            {{ item.title }}
        </router-link>
    </li>
</template>
<script>
export default {
    name: 'NavItem',
    props: {
        item : Object
    }
}
</script>
<style scoped>
    a{
        color: #333;
    }
    a:hover{
        color: #888;
        transition: color .5s;
    }
</style>