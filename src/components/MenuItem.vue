<template>
    <div class="menu-item m-1" v-on:click="clicked">
        <img class="menu-item_img" :src="item.img"/>
        <h4 class="menu-item_title">
            {{ item.title }}
        </h4>
        <div class="menu-item_description" >
            {{ item.description }}
        </div>
    </div>
</template>

<script>
export default {
    name: "MenuItem",
    props: {
        item: Object
    },
    methods: {
        clicked() {
            return alert("OK");
        }
    }
}
</script>

<style scoped>
.menu-item{
    display: flex;
    flex-direction: column;
    flex-basis: 100%;
    justify-content: start;
    align-items: stretch;
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
.menu-item_img{
    width:100%;
    border-bottom: 1px solid #888;
    min-height: 14rem;
}
.menu-item_title{
    font-weight: 700;
    background-color: #e8e8e8;
    height: 2.5rem;
    margin: 0;
    padding-top: 1rem;
}
.menu-item_description{
    padding: .5rem;
}
</style>