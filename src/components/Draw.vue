<template>
    <canvas ref="canvas" :width="widthCanvas" :height="heightCanvas" v-on:click="clickCanvas($event)">
    </canvas>
</template>
<script>
export default {
    data: function(){
        return {
            range: []
        }
    },
    methods : {
        draw: function(){ 
            let ctx = this.$refs.canvas.getContext('2d');
            let w = this.$refs.canvas.width;
            let h = this.$refs.canvas.height;
            ctx.fillStyle = "gray";
            ctx.fillRect(0, 0, w, h);
            let x = w - 400;
            let y = h - 100;
            let bx = 200;
            let by = 50;
            ctx.clearRect(bx, by, x, y);
            
            ctx.strokeStyle = "black";
            ctx.fillStyle = "black";
            ctx.strokeRect(bx, by, x, y);
            ctx.fillRect(x / 3 + bx - 50, y - by - 150, 20, 250);
            ctx.fillRect(x / 3 * 2 + bx, y - by - 150, 20, 250);
            ctx.fillRect(x / 3 * 2 + bx + 100, y - by - 150, 120, 250);
            ctx.fillRect(x + 100, by + 170, 100, 10);
            //////
            ctx.strokeRect(bx, y - by - 100, 100, 200);
            ctx.strokeRect(bx + 176, y - by - 100, 100, 200);
            ctx.strokeRect(bx + 298, y - by - 100, 150, 200);
            ctx.strokeRect(bx + 503, y - by - 100, 150, 200);
        },
        clickCanvas(event){
            
        }
    },
    computed:{
        widthCanvas(){
            return window.innerWidth * 0.9 + 'px';
        },
        heightCanvas(){
            return window.innerHeight * 0.8 + 'px';
        }
    },
    mounted(){
        this.draw()
    }
}
</script>