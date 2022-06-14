<template>
  <div class="about">
    <img src="./images/about.jpg" class="img-fluid">
    <p class="para">ABOUT US</p>
    <AboutView2 />
  </div>
</template>

<script>
import AboutView2 from './AboutView2'
export default{
  name:'AboutView',
  components:{
    AboutView2,
  },
  data(){
    return{
    }
  },
}
</script>

<style scoped>
.about img{
  max-width:100%;
  min-height:500px;
  opacity:0.8;
}
.para{
  left: 0;
  position: absolute;
  text-align: center;
  top: 38%;
  width: 100%;
  font-size:25px;
  font-weight: bold;
  color:black;
}

@media only screen and (max-width:500px){

}
</style>