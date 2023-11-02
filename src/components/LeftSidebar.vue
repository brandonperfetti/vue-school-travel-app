<template>
  <ul>
    <li><AppLink :to="{ name: 'protected' }">Dashboard</AppLink></li>
    <li><AppLink :to="{ name: 'invoices' }">Invoices</AppLink></li>
  </ul>
</template>

<style scoped>
ul {
  background: white;
  padding: 10px;
  list-style: none;
  margin-right: 20px;
}
li {
  margin: 10px;
}
</style>
