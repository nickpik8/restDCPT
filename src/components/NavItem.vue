<template>
    <li class="m-2">
        <a :href="item.href">
            {{ item.title }}
        </a>
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