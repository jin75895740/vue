<template>
  <div>
    <input type="button" @click="reg()" value="注册">
    <input type="button" @click="login()" value="登录">
  </div>
</template>

<script>
  export default {
    name: 'Login',
    methods: {
      reg: function() {
        this.$router.push('/home/list');
      },
      login: function() {

      }
    }
  };
</script>

<style scoped>

</style>
