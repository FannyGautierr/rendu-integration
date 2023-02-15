<script setup>
defineProps({
  name:String,
  status:String,
  Img:String,
  Price:String,
  PriceColor:String,
  Date:String,
})

</script>


<template>

  <div>
    <img src="{{ Img }}" alt="">
    <div class="name-status">
      <p><b>{{ name }}</b></p>
      <p>{{ status }}</p>
    </div>
    <div class="price-date">
      <p class="{{ PriceColor }}">{{ Price }}</p>
      <p>{{ Date }}</p>
    </div>
  </div>

</template>



<style scoped>
.red{
  color: red;
}

.green{
  color: green;
}
</style>