<template>
    <div class="box">
    <div>  {{msg}}</div>
      <button @click='add'>增加1</button>
      <button @click='reduce'>减小1</button>
    </div>
</template>

<script>
export default {
    props: {

    },
    data() {
        return {
          msg:0
        };
    },
    methods: {
      add(){
        this.msg++;
        this.$emit('liu',this.msg);
      },
      reduce(){
        if(this.msg>0){
             this.msg--;
        this.$emit('liu',this.msg);
        }

      }
    },
    components: {

    },
};
</script>

<style scoped >
  .box{
    width: 200px;
    border: 1px solid green;
    padding: 10px 10px;
    margin: 0 auto;
  }
  .box button{
    /* width: 30px; */
    height: 30px;
    background-color: blue;
    border: none;
    color: #fff;
    margin-top: 20px;
  }
</style>
