<template>
  <div class="student_id">
    <h2>{{name}}</h2>
    <div calss="link">
      <NuxtLink to="/students">生徒一覧へ戻る</NuxtLink>
      |
      <NuxtLink to="/">トップページへ</NuxtLink>
    </div>
  </div>
</template>


<script>
export default {
  validate({ params, store }) {
    return store.state.students.some((student) => student.id === params.id);
  },
  data(){
    return {
      name:null,
      id:this.$route.params.id
    }
  },
  created(){
      const currentUser = this.$store.state.students.find(v => v.id === this.id);
      this.name = currentUser.name;
  }
};
</script>


<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.link{
  display: flex;
}
</style>