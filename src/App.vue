<script setup>

import Sidebar from "./components/Sidebar.vue";
import SearchBar from "./components/SearchBar.vue";
import TotalBalance from "./components/TotalBalance.vue";
import Graph from "./components/Graph.vue";
import RecentTransactionsBig from "./components/RecentTransactionsBig.vue";
import RecentTransactionsLittle from "./components/RecentTransactionsLittle.vue";
import AssetsCard from "./components/AssetsCard.vue";
import {onMounted, ref} from "vue";

const showSideBar = ref(false)

function toggle(){
  showSideBar.value=!showSideBar.value
  document.addEventListener("click",function (){

  })
}

onMounted(()=>{

  showSideBar.value = window.innerWidth > 900;
  window.addEventListener('resize',function (){
    showSideBar.value = window.innerWidth > 900;

  })
})

</script>

<template>
  <div class="header">
    <Sidebar v-if="showSideBar" :funtion="toggle"/>
    <div class="little-div">
    <SearchBar :funtion="toggle"/>
      <div class="flex-row main-layout">
        <div class="flex-col center-layout">
          <!-- !!!--->
          <TotalBalance/>
          <Graph/>
          <div class="flex-row text-white recent-transactions poppins"><p>Recent Transactions </p><p class="text-grey">See all coins</p></div>
          <RecentTransactionsBig
              logo="src/assets/crypto/bitcoin-orange.svg"
              name="Bitcoin"
              acronym="BTC"
              marketColor="blue"
              changeColor="green"
              worm="src/assets/graph/firstWorm.svg"
          />
          <RecentTransactionsBig
              logo="src/assets/crypto/Etherium-white.png"
              name="Etherum"
              acronym="ETH"
              marketColor="violet"
              changeColor="red"
              worm="src/assets/graph/secondWorm.svg"
          />

        </div>
        <div class="flex-col right-sidebar">

          <!-- !!!--->
          <div class="little-recent-transactions">
            <h2 class="text-white poppins">Recent Transactions</h2>

            <RecentTransactionsLittle
                name="Usdt"
                img="src/assets/crypto/Tether.png"
                Price="+$3,546"
                color="green"
                hour="Today, 13:45 pm"
                status="Received"
            />
            <RecentTransactionsLittle
                name="BNB"
                img="src/assets/crypto/BNB.png"
                Price="+ 0.7546"
                color="green"
                hour="Today, 5:45 am"
                status="Buy"
            />
            <RecentTransactionsLittle
                name="Lite Coin"
                img="src/assets/crypto/Logo.png"
                Price="- $0.7546"
                color="red"
                hour="Today 7:55 am"
                status="Withdrawal"
            />
            <RecentTransactionsLittle
                name="Bitcoin"
                img="src/assets/crypto/Group.png"
                Price="+ $2.7546"
                color="green"
                hour="Today 8:55 am"
                status="Received"
            />
            <RecentTransactionsLittle
                name="Etherum"
                img="src/assets/crypto/Etherium icon.png"
                Price="+ $1.646"
                color="green"
                hour="Today, 13:45 pm"
                status="Received"
            />
            </div>
            <div class="assets">
              <h2 class="text-white poppins">Assets</h2>

            <AssetsCard
                name="Bitcoin"
                logo="src/assets/crypto/bitcoin-white.png"
                gradient="gradient-1"
                acronym="BTC"
                value="121,6450.45"
            />
            <AssetsCard
                name="Etherum"
                logo="src/assets/crypto/Etherium icon.png"
                gradient="gradient-2"
                acronym="ETH"
                value="143,850.45"
            />

        </div>
      </div>
    </div>
  </div>
</div>



</template>

<style scoped>
.header{
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  width: 100vh;
}

.main-layout{
  flex-direction: row;
  justify-content: center;
  gap: 100px;

}

.center-layout{
  margin-top: 50px;
  padding: 20px;
  gap: 20px;

  height: 100vh;

}
.right-sidebar{
  justify-content: space-between;

  margin-right: 2rem;
  height:90vh;
  margin-top: 60px;
  gap: 100px;
  overflow: scroll;


}
.little-recent-transactions{
  display: flex;
  gap: 20px;
  flex-direction: column;
  /*margin-top: 55px;*/

}

.recent-transactions{
  justify-content: space-between;
  padding: 0 1rem;
}
.little-div{

}
.assets{
  display: flex;
  flex-direction: column;
  gap: 20px;
}
@media screen and (max-width:1500px) {
  .main-layout{
    display: flex;
    flex-direction: column;
    gap: 0;
  }
.right-sidebar{
  overflow: visible;
}
.center-layout{
  width: fit-content;
}

}
@media screen and (max-width:1200px) {
  .main-layout{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0;
  }
  .center-layout{
    width: fit-content;

  }
  .right-sidebar{

    justify-content:space-evenly;

    height: fit-content;
    align-items: flex-start;
    gap:20px;
  }
  .assets{
    display: flex;
    flex-direction: column;
    gap: 20px;

  }

}

@media screen and (max-width:900px) {
.right-sidebar{
overflow: visible;
}
}

@media screen and (max-width:700px) {
  .right-sidebar{
    margin-top: 0;
    flex-direction: column;
    width: 80%;
    margin-left: 10px;

  }
  .header{
    display: flex;
    flex-direction: column;
    width: 100%;
  }
  .main-layout{
    flex-direction: column;
    width: 25rem;
  }

  .center-layout{
    width:25rem;
    overflow: visible;
    height: auto;
    align-items: center;
  }

  .recent-transactions{
    justify-content: flex-start;
    gap: 2rem;
  }
  .little-recent-transactions{
    overflow: visible;
    width: 25rem;
    margin-top: 1px;
  }
  .little-div{
    width: 25rem;
  }
}

</style>
