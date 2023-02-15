<script setup>

defineProps({
  logo: String,
  name: String,
  acronym: String,
  changeColor:String,
  marketColor:String,
  worm:String


})

</script>


<template>
  <div class="big-transactions poppins">
    <img :src="logo" alt="">
    <div>
      <p>{{name}}</p>
      <p>{{acronym}}</p>
    </div>
    <div>
      <p>Market Cap</p>
      <p :class="marketColor">$40,243.70</p>
    </div>
    <div>
      <p>24h change</p>
      <p :class="changeColor">+1,56</p>
    </div>

    <img :src="worm" alt="">
    <div class="trade-button"><p>Trade</p></div>

  </div>
</template>


<style scoped>

.big-transactions{
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
  background: rgba(32, 35, 43, 0.7);
  border-radius: 30px;
  color: white;

}
.red{
  color: red;
}

.violet{
  color: violet;
}
.blue{
  color: blue;
}
.green{
  color: green;
}
.trade-button{
  background-color: #0D0C0C;
  color: #FFFFFF;
}




</style>