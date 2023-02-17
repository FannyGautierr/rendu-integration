
<script>
export default {
  name: "TotalBalance"
}
</script>


<template>
<div class="emo">
  <div class="flex-col text-white poppins">
    <h2 >Total Balance</h2>
    <div class="flex-row gap">
        <p>0.97894652 </p>
        <div class="yellow">BTC</div>
    </div>
    <p>$40,123.56</p>
  </div>


  <div class="flex-row menu text-white poppins">
    <div class="active">Portfolio</div>
    <div>Funding</div>
    <div>Assets</div>
    <div>P2P</div>

  </div>

</div>
</template>



<style scoped>
.active{
  background-color: #0D0C0C;
  border-radius: 17px;
  padding: 5px 20px;
}
.emo{
  display: flex;
  flex-direction: row;
  gap: 90px;
  align-items: center;
}
.menu{
  background-color: #292727;
  padding: 10px 20px 10px 10px;
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
  width: fit-content;
  border-radius: 17px;
}
.yellow{
  background-color: #FAFF00;
  border-radius: 8px;
  padding: 4px 9px;
  color: black;
  font-weight: normal;

}

.gap{
  align-items: center;
  gap: 10px;
}
@media screen and (max-width:700px) {
  .emo{
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
  }
}
</style>