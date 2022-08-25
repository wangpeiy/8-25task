<template>
  <div>
    <p>请选择你喜欢的专栏：</p>
    <label v-for="(item,index) in arr " :key="index" >
      <input type="checkbox" v-model="newarr" :value="item">
      <span>{{ item }}</span> &nbsp;
    </label>
    <br><br>
    <ul>
      <li v-for="(item,index) in newarr" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr:["科幻", "喜剧", "动漫", "冒险", "科技", "军事", "娱乐", "奇闻"],
      newarr: []
    }
  },
}
</script>

<style>

</style>
