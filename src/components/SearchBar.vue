<template>
<div class="search-bar">

  <h2 class="name">Hi, Rogers </h2>

  <div class="search-input">
    <img src="src/assets/search-logo.svg" alt="">
    <p>Search ...</p>
  </div>

  <div class="notif-and-user">
  <img src="src/assets/notif-logo.svg" alt="">
  <img src="src/assets/user-profile.png" alt="">
  </div>


</div>
</template>

<script>
export default {
  name: "SearchBar"
}
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
  justify-content: space-between;
  align-items: center;
  margin-top: 50px;
  gap: 100px;

}
.notif-and-user{
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  gap: 200px;
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
</style>