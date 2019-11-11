<template>
  <div>
    <ul class="lis">
      <li v-for="(item,index) in arr1" :key="index">
        <img :src="item.imgUrl1" alt="">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    arr1: {
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

<style scoped >
.lis{
  margin-left: 100px;
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  padding: 10px 10px;
}
.lis li{
  margin-right: 20px;
   border: 1px solid #ccc;
   border-radius: 5px;
   padding: 10px;
}
</style>
