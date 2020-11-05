<template>
    <div>
        <p>
            {{ textPage }}
            
        </p>
        <img :src="img.link" class="img-home"/>
        {{ img.width }}
    </div>
</template>
<script>
export default {
    data(){
        return{
            textPage: `Это главная страница сайта нашего ресторана. 
            Вы можете посмотреть наше уникальное меню, в лучших традициях классической и современной кухни. Забронировать столик в 
            разделе бронирования. Или связаться с нами. Где мы находимся, карта, телефоны и прочее указано в разделе контакты. 
            Мы страемся для Вас!`,
            img:{
                link: require("../assets/images/home.jpg")
            }
        }
    }
}
</script>
<style scoped>
.img-home{
    max-width: 100%;
}
</style>