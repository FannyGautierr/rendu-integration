<script setup>
defineProps({
   gradient:String,
   logo:String,
   name:String,
   value:String,
   acronym:String,

})

</script>


<template>

  <div class="flex-col cards" :class="gradient">
    <div class="flex-col name">
      <img :src="logo" alt="">
      <p>{{ name }}</p>
    </div>
    <div class="flex-row value">
      <p>{{ value }}</p>
      <p>{{ acronym }}</p>
    </div>

  </div>

</template>




<style scoped>


.value{
  justify-content: space-between;
  font-size: 24px;
}

.name{
  gap: 20px;
  font-size: 19px;
}

.gradient-1{
  background:  linear-gradient(98.73deg, #611D8D 35.75%, #2F7EC1 73.26%);
  color: #FFFFFF;
}

.gradient-2{
  background: linear-gradient(99.56deg, #FAFF00 35.82%, #29ABE2 64.75%, rgba(255, 255, 255, 0.7) 91.33%);
  color: black;
}
.cards{
  border-radius: 30px;
  font-family: 'Poppins', sans-serif;
  padding:2rem 3rem ;
  width: 24rem;
  height: fit-content;

}

img{
  width: 5rem;
}
</style>