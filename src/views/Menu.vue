<template>
    <div class="menu">
        <MenuItem 
            v-for="item in menu" :key="item.id"
            v-bind:item="item"
        />
    </div>
</template>

<script>
import MenuItem from '@/components/MenuItem'
export default {
    data(){
        return {
            menu: [
                {
                    id: '1', 
                    title: 'Закуски', 
                    img: require('../assets/catalog/snacks_small.jpg'), 
                    description: 'Горячие и холодные закуски'
                },
                {
                    id: '2', 
                    title: 'Салаты', 
                    img: require('../assets/catalog/salad_small.jpg'), 
                    description: 'Салаты приготовленные нашим шеф-поваром'
                },
                {
                    id: '3', 
                    title: 'Супы', 
                    img: require('../assets/catalog/soup_small.jpg'), 
                    description: 'Рекомендуем наш фирменный овощной крем - суп'
                },
                {
                    id: '4', 
                    title: 'Домашняя еда', 
                    img: require('../assets/catalog/homefood_small.jpg'), 
                    description: 'Как дома, котлетки, блины и пироги как у бабушки'
                },
                {
                    id: '5', 
                    title: 'Мясные блюда', 
                    img: require('../assets/catalog/meat_small.jpg'), 
                    description: 'Исключительно мясные блюда из телятины, баранины и свинины'
                },
                {
                    id: '6', 
                    title: 'Блюда из рыбы и морепродуктов', 
                    img: require('../assets/catalog/sea_small.jpg'), 
                    description: 'Большой ассортимент рыбных блюд'
                },
                {
                    id: '7', 
                    title: 'Гриль-меню', 
                    img: require('../assets/catalog/grill_small.jpg'), 
                    description: 'Стейк, соус и овощи - гриль.'
                },
                {
                    id: '8', 
                    title: 'Десерты', 
                    img: require('../assets/catalog/desert_small.jpg'), 
                    description: 'Сладкие и диетические десертные блюда'
                }
            ]
        }
    },
    components: {
        MenuItem
    }
}
</script>

<style scoped>
.menu{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
}
</style>