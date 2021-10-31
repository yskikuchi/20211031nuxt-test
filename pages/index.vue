<template>
  <div class="container">
    <div>
      <h2>生徒一覧</h2>
      <NuxtLink to="/students">生徒の情報を見る</NuxtLink>
    </div>
    <div>
      <h2>管理者</h2>
      <NuxtLink to="/management">管理画面を見る</NuxtLink>
    </div>
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
