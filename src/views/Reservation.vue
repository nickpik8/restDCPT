<template>
    <canvas ref="canvas" width="600px" height="500px" @:onload="load">
    </canvas>
</template>
<script>
export default {
    methods : {
        load: function(){
            let ctx = this.$refs.canvas.getContext('2d');
            ctx.fillStyle = "green";
            ctx.fillRect(10, 10, 100, 100);
        }
    }
}
</script>