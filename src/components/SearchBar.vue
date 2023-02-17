<template>
<div class="search-bar">
  <div class="burger-menu" @click="funtion">
    <ion-icon name="menu-outline" style="color: #FFFFFF"></ion-icon>
  </div>
  <h2 class="name">Hi, Rogers </h2>

  <div class="search-input non-active" >
    <img src="src/assets/search-logo.svg" alt="" class="logo-search">
    <p class="text-search" >Search ...</p>
  </div>

  <div class="notif-and-user">
  <img src="src/assets/notif-logo.svg" alt="">
  <img src="src/assets/user-profile.png" alt="">
  </div>


</div>
</template>

<script setup >
import {onMounted} from "vue";

const {funtion}=defineProps(["funtion"])

</script>

<style scoped>
.name {
  color: #FFFFFF;
  font-family: 'Poppins', sans-serif;
  font-weight: lighter;
}
.burger-menu{
  position: absolute;
  z-index: 10;
  font-size: 100px;
}
.search-bar{
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 35px;
  gap: 150px;
  width: 50rem;
  justify-content: space-evenly;
  background-color: #0000;

}
.notif-and-user{
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 100px;
  margin-left: 20px;
}
.search-input{
  background-color: #FFFFFF;
  border-radius: 15px;
  width: 30rem;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  padding: 5px 23px ;
  gap: 15px;
  font-family: 'Poppins', sans-serif;
  font-weight: lighter;
}
@media screen and (max-width:1500px) {

  .notif-and-user{
    gap: 50px;
  }

}
@media screen and (max-width:900px) {



}

@media screen and (max-width:700px) {
 .search-input{
   width: 100%;
   text-align: center;
   align-items: center;

   height: fit-content;
   border-radius: 20px;
   grid-row: 2;
   grid-column: 1/4;
 }
.logo-search{

}

.search-bar{
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-template-rows: repeat(2,1fr);
  width: 100%;
  gap: 10px;
  padding: 20px;

}
.notif-and-user{
  gap: 40px;
  grid-column: 2/4;
  justify-content: space-between;
}


}
</style>