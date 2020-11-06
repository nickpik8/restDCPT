<template>
    <canvas ref="canvas" :width="widthCanvas" :height="heightCanvas" v-on:click="clickCanvas($event)">
    </canvas>
</template>
<script>
export default {
    data(){
        return {
            range: {
                x: {
                    begin: [],
                    end: []
                },
                y: {
                    begin: [],
                    end: []
                } 
            }
        }
    },
    methods : {
        draw: function(){ 
           /* let ctx = this.$refs.canvas.getContext('2d');
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
            this.range.x.begin.push(bx);
            this.range.x.end.push(bx + 100);
            this.range.x.begin.push(bx + 176);
            this.range.x.end.push(bx + 176 + 100);
            this.range.x.begin.push(bx + 298);
            this.range.x.end.push(bx + 298 + 150);
            this.range.y.begin.push(y - by - 100);
            this.range.y.end.push(y - by);
            this.range.y.begin.push(y - by - 100);
            this.range.y.end.push(y - by);*/
        },
        clickCanvas(event){
         /*   let ctx = this.$refs.canvas.getContext('2d');
            let x = event.x;
            let y = event.y;
            for (let i = 0; i < 2; i++){
                if (x > this.range.x.begin[i] && x < this.range.x.end[i] && y > this.range.y.begin[i] && y < this.range.y.end[i]){
                    ctx.fillStyle = "green";
                    ctx.fillRect(this.range.x.begin[i], this.range.y.begin[i], this.range.x.end[i] - this.range.x.begin[i], this.range.y.end[i] - this.range.y.begin[i]);
                }
            }*/
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