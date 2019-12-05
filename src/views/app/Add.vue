<template>
  <div>
    Add view
    <div>标题: <input type="text" v-model="title"></div>
    <div>内容: <input type="text" v-model="content"></div>
    <div><input type="button" value="保存" @click="save()"></div>
  </div>
</template>

<script>
  import store from '@/store/index.js';

  export default {
    name: 'Add',
    data: function () {
      return {
        title: null,
        content: null
      }
    },
    methods: {
      save: function () {
        if(this.title && this.content) {
          store.commit('addItem', {
            title: this.title,
            content: this.content
          });
          this.title = null;
          this.content = null;
          this.$router.push('/home/list');
        } else {
          alert('不能为空！');
        }
      }
    }
  };
</script>

<style scoped>

</style>
