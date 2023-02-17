<script setup>

import Sidebar from "./components/Sidebar.vue";
import SearchBar from "./components/SearchBar.vue";
import TotalBalance from "./components/TotalBalance.vue";
import Graph from "./components/Graph.vue";
import RecentTransactionsBig from "./components/RecentTransactionsBig.vue";
import RecentTransactionsLittle from "./components/RecentTransactionsLittle.vue";
import AssetsCard from "./components/AssetsCard.vue";
</script>

<template>
  <div class="header">
    <Sidebar/>
    <div>
    <SearchBar/>
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
  gap: 80px;
}

.center-layout{
  margin-top: 50px;
  padding: 20px;
  gap: 20px;
  overflow: scroll;
  height: 100vh;
}
.right-sidebar{
  justify-content: space-between;
  overflow: scroll;
margin-right: 2rem;
  height:100vh;
}
.little-recent-transactions{
  display: flex;
  gap: 20px;
  flex-direction: column;
  margin-top: 55px;
}

.recent-transactions{
  justify-content: space-between;
  padding: 0 1rem;
}

@media screen and (max-width:700px) {
  .header{
    display: flex;
    flex-direction: column;
  }
  .main-layout{
    flex-direction: column;
  }

  .center-layout{
    width:25rem;
    overflow: visible;
    height: auto;
  }

  .recent-transactions{
    justify-content: flex-start;
    gap: 2rem;
  }
  .little-recent-transactions{
    overflow: visible;
    width: 25rem;
  }
}

</style>
