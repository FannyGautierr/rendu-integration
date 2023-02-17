


<template>
<div class="search-bar">

  <h2 class="name">Hi, Rogers </h2>

  <div class="search-input non-active" @click="handleClick">
    <img src="src/assets/search-logo.svg" alt="" class="logo-search">
    <p class="text-search" >Search ...</p>
  </div>

  <div class="notif-and-user">
  <img src="src/assets/notif-logo.svg" alt="">
  <img src="src/assets/user-profile.png" alt="">
  </div>


</div>
</template>

<script >
export default {

  methods: {
    handleClick(event) {
      // 👇 Change style
      console.log("hauhuiz")
      event.currentTarget.classList.toggle('non-active');
      event.currentTarget.classList.toggle('active');
    },
  },
};
</script>

<style scoped>
.name {
  color: #FFFFFF;
  font-family: 'Poppins', sans-serif;
  font-weight: lighter;
}
.search-bar{
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 35px;
  gap: 100px;

}
.notif-and-user{
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 190px;
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

@media screen and (max-width:700px) {
 .search-input{
   width: 4rem;
   text-align: center;
   align-items: center;
   justify-content: center;
   height: fit-content;
   border-radius: 20px;

 }
.logo-search{

}
.text-search{
  display: none;
}
.search-bar{
  width: 100vh;
  gap: 10px;
  margin-left: 20px;
}
.notif-and-user{
  gap: 40px;
}
.active{
  width: 10rem;
  justify-content: flex-start;

}
.active::after{
  content: "search";
  font-weight: lighter;
  color: grey;
}
.non-active{
  width: 4rem;
  text-align: center;
  align-items: center;
  justify-content: center;
  height: fit-content;
  border-radius: 20px;
}
}
</style>