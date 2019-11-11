<template>
  <div class="hello">
    <Movie :arr='arr'></Movie>
    <Picture :arr1='arr1'></Picture>
    <!-- <h1>{{msg}}</h1> -->
    <Click @liu='fn'></Click>
  </div>
</template>

<script>
import Movie from './Movie'
import Picture from './Picture'
import Click from './Click'
export default {
  name: 'HelloWorld',
  data () {
    return {
      arr:[
        {imgUrl:'/static/img/pic_01.jpg',title:'风景狙击手',p1:'成品:10',p2:'作品:10'},
        {imgUrl:'/static/img/pic_02.jpg',title:'风景狙击手',p1:'成品:10',p2:'作品:10'},
        {imgUrl:'/static/img/pic_03.jpg',title:'风景狙击手',p1:'成品:10',p2:'作品:10'},
        {imgUrl:'/static/img/pic_04.jpg',title:'风景狙击手',p1:'成品:10',p2:'作品:10'},
        {imgUrl:'/static/img/pic_05.jpg',title:'风景狙击手',p1:'成品:10',p2:'作品:10'},
        {imgUrl:'/static/img/pic_06.jpg',title:'风景狙击手',p1:'成品:10',p2:'作品:10'}
        ]
        ,arr1:[
          {imgUrl1:'/static/img/1.jpg'},
          {imgUrl1:'/static/img/2.jpg'},
          {imgUrl1:'/static/img/3.jpg'},
          {imgUrl1:'/static/img/4.jpg'},
          {imgUrl1:'/static/img/5.jpg'},
          {imgUrl1:'/static/img/6.jpg'},
          {imgUrl1:'/static/img/7.png'},
          {imgUrl1:'/static/img/8.png'}
        ],
        msg:0
    }
  },
  components:{
    Movie,Picture,Click
  },
  methods:{
    fn(v){
      this.msg=v;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
