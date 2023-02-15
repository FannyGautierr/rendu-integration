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
    <RecentTransactionsLittle
    name="Usdt"
    img="./assets/crypto/Tether.png"
    price="+$3,546"
    price-color="green"
    date="Today, 13:45 pm"
    status="Received"
    />
    <AssetsCard/>
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
