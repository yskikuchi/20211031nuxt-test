<template>
  <div class="students">
    <h2>生徒一覧</h2>
    <ul>
      <li v-for="student in $store.state.students" :key="student.id">
        <NuxtLink :to="{path:`students/${student.id}`}">{{student.name}}</NuxtLink>
      </li>
    </ul>
    <NuxtLink to="/">戻る</NuxtLink>
  </div>
</template>


<script>
export default {

};
</script>


<style>
.students {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>