<template>
  <div class="management">
    <h2>生徒管理ページ</h2>
    <table>
      <tr>
        <th>名前</th>
        <th>ID</th>
      </tr>
      <tr v-for="student in $store.state.students" :key="student.id">
        <td>{{student.name}}</td>
        <td>{{student.id}}</td>
      </tr>
    </table>
    <NuxtLink to="/">戻る</NuxtLink>
  </div>
</template>


<script>
export default {
};
</script>


<style>
.management {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>