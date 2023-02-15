<script setup>
defineProps({
  name:String,
  status:String,
  img:String,
  Price:String,
  color:String,
  hour:String,
})

</script>


<template>

  <div class="recent-transactions">

    <div class="photo-name">
    <img :src="img" alt="">
    <div class="name-status">
      <p><b>{{ name }}</b></p>
      <p>{{ status }}</p>
    </div>
    </div>

    <div class="price-date">
      <p :class="color">{{ Price }}</p>
      <p>{{ hour }}</p>
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

.recent-transactions{
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 100px;
}
.name-status ,.price-date{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;

}
.photo-name{
  display: flex;
  flex-direction: row;
  gap: 28px;
}

*{
  color: #FFFFFF;
  font-family: 'Poppins', sans-serif;
}
</style>