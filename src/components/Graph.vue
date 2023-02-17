<template>
 <img src="src/assets/graph/graph.png" alt="">
 <!-- <canvas id="bitcoin-chart" ref="ctx"></canvas> -->
</template>

<script >

export default {
  name: "Graph",
 /* mounted() {
    const ctx = this.$refs.ctx.getContext('2d');
    new Chart(ctx, {
      type: 'line',
      data: {
        labels:["5Nov","6Nov","7Nov","8Nov","9Nov","10Nov","11Nov","12Nov","13Nov","14Nov","15Nov"],
        datasets:[
          {
            label:'ETH',
            data:[150,600,300,400],
            borderColor: 'rgb(75, 192, 192)',
          }
        ]
      },
      options: {},
    });
  }*/
}

</script>

<style scoped>
img{
  width: 40rem;
}
@media screen and (max-width:700px) {
img{
  width: 22rem;
}
}
</style>