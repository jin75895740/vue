<template>
  <div>
    List view
    <ul>
      <li v-for="(item,index) in pageList" :key="index">
        {{item.title}}-{{item.content}}
      </li>
    </ul>
  </div>
</template>

<script>
  import store from '@/store/index.js';
  export default {
    name: 'List',
    computed: {
      pageList: function () {
        return store.state.lists;
      }
    }
  };
</script>

<style scoped>

</style>
