<template>
    <div class="menu-item m-1">
        <img class="menu-item_img" :src="item.img"/>
        <div class="menu-item_title">
            {{ item.title }}
        </div>
        <div class="menu-item_description">
            {{ item.description }}
        </div>
    </div>
</template>

<script>
export default {
    name: "MenuItem",
    props: {
        item: Object
    }
}
</script>

<style scoped>
.menu-item{
    flex-basis: 100%;
    border: 1px dashed #888;
}
@media (min-width: 400px){
    .menu-item{
        flex-basis: 40%;
    }
}
@media (min-width: 768px){
    .menu-item{
        flex-basis: 30%;
    }
}
@media (min-width: 1200px){
    .menu-item{
        flex-basis: 20%;
    }
}
.menu-item_title{
    font-weight: 700;
}
.menu-item_img{
    width:100%;
    border-bottom: 1px solid #888;
    min-height: 14rem;
}
.menu-item_description{
    padding: .5rem;
}
</style>