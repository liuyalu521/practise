<template>
  <div class="box">
    <p>摄影社区热门小镇</p>
    <ul class="lis">
      <li v-for="(item,index) in arr" :key="index">
        <img :src="item.imgUrl" alt />
        <div class="text">
          <p>{{item.title}}</p>
          <p>{{item.p1}}</p>
          <p>{{item.p2}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Movie",
  props: {
    arr: {
      type: Array
    }
  },
  data() {
    return {};
  },
  methods: {},
  components: {}
};
</script>

<style scoped>
*{
  padding: 0;
  margin: 0;
}
.box {
  width: 600px;
  padding: 20px 21px;
  margin: 0 auto;
  border: 1px solid #ccc;
}
.box>p{
  text-align: left;
  margin-bottom: 50px;
}
.lis{
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  justify-content: space-between;
}
.lis li{
  display: flex;
  height: 100px;
  margin-right:30px;
}
.lis li img{
  width: 60px;
  height: 60px;
  margin-right: 10px;
  border:1px solid #ccc;
}
.lis li div{
  flex:1;
  font-size: 12px;
  color: #ccc;
}
.text p:nth-child(1){
font-weight: bolder;
color: #5C88AC;
}
</style>
