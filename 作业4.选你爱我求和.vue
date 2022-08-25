<template>
  <div>
    <label v-for="(item,index) in arr " :key="index" >
      <input type="checkbox" v-model="newArr" :value="item">
      <span>{{ item }}</span> &nbsp;
    </label>
    <p> 你选中的元素累加的和为： {{ sum }} </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr:[9, 15, 19, 25, 29, 31, 48, 57, 62, 79, 87],
      newArr:[]
    }
  },
  computed:{
    sum(){
      return this.newArr.reduce((acc,item) => {
        return acc += item
      },0);
    }
  }
}
</script>

<style>

</style>
