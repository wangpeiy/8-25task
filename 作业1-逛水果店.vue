<template>
  <div>
    <p>欢迎光临_vue开发的收银系统_水果店</p>
    <table border="1">
     <thead>
      <th>
        苹果10￥/斤，折扣 8折
      </th>
      </thead>

      <tbody>
        <tr>请输入你要购买的斤数：<input type="number" v-model.number="num"></tr>
        <tr><button @click="compute">结账买单</button></tr>
        <tr>结账单：总价：<span>{{ totalPrice }}￥元</span> 折后价：<span>{{ zhehouPrice }}￥元</span> 省了：<span>{{ delPrice }}￥元</span></tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num:0,
      totalPrice:0,
      zhehouPrice:0,
      delPrice:0
    }
  },
  methods: {
    compute(){
      this.totalPrice = this.num * 10;
      this.zhehouPrice = this.totalPrice * 0.8;
      this.delPrice = this.totalPrice - this.zhehouPrice
    }
  },
}
</script>

<style>

</style>
