<template>
  <div id="side-bar">


<div class="logo">
  <p>
  <img src="src/assets/mLogo.svg" alt="">
  <span>inance</span>
  </p>
</div>
<div class="menu-items-and-dash">
  <div class="dashboard">
    <img src="src/assets/dashboard-logo.svg" alt="">
    <p>Dashboard</p>
  </div>

  <div class="menu">
    <div class="menu-items">
      <img src="src/assets/invoices-logo.svg" alt="">
      <p>Invoices</p>
    </div>

    <div class="menu-items">
      <img src="src/assets/clients-logo.svg" alt="">
      <p>Clients</p>
    </div>

    <div class="menu-items">
      <img src="src/assets/products-logo.svg" alt="">
      <p>Products</p>
    </div>

    <div class="menu-items">
      <img src="src/assets/messages-logo.svg" alt="">
      <p>Messages</p>
    </div>

    <div class="menu-items">
      <img src="src/assets/settings-logo.svg" alt="">
      <p>Settings</p>
    </div>

    <div class="menu-items">
      <img src="src/assets/help-logo.svg" alt="">
      <p>Help</p>
    </div>

  </div>
</div>
    <div class="log-out menu-items">
      <img src="src/assets/logout-logo.svg" alt="">
      <p>Log Out</p>
    </div>
</div>
</template>

<script>
export default {
  name: "sidebar"
}
</script>

<style scoped>

.log-out{

}

#side-bar{
  padding: 3rem;
  display: flex;
  flex-direction: column;
  gap: 100px;
  width: fit-content;
}

.logo{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 4px;
  font-size: 36px;
  width: fit-content;
  color: #FFFFFF
}
.menu-items-and-dash{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 25px;
}
.dashboard{
  background: linear-gradient(266.37deg, #FAFF00 -5.82%, #FAFF00 15.95%, #1970D6 41.2%, #6C1182 72.88%);
  font-family: 'Poppins', sans-serif;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 10px;
  width: fit-content;
  border-radius: 17px;
  font-size: 25px;
  font-weight: lighter;
  padding: 10px 29px;
  color: black;
}
.menu{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  width: fit-content;
  align-items: flex-start;
  gap: 28px;
}

.menu-items{
  font-family: 'Poppins', sans-serif;
  font-weight: normal;
  display: flex;
  flex-direction: row;
  gap: 10px;
  align-items: center;
  justify-content: flex-start;
  color: black;
  color: rgba(255,255,255,0.8);
  background-color: black;
}
</style>