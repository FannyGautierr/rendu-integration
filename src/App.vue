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
    <SearchBar/>
  </div>

  <div class="main">
    <TotalBalance/>
    <Graph/>
    <RecentTransactionsBig/>
  </div>

  <div class="aside">
      <div class="little-recent-transactions">
        <H2 class="text-white poppins">Recent Transactions</H2>
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

</template>

<style scoped>
.header{
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  width: 100%;
}
</style>
