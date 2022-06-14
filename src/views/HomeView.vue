<template> 
  <div class="home">
   <!-- Carousel -->
    <div class="row smallscreen">
      <div class="col-sm-12">
      <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-indicators move">
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active imageslider">        
            <img src="./images/home1.jpg" class="img-fluid" alt="...">
            <p class="para">Welcome To Guybrand Limited</p>
          </div>
          <div class="carousel-item imageslider">
            <img src="./images/home2.jpg" class="img-fluid" alt="...">
            <p class="para">Design, Planning & Build</p>
          </div>
          <div class="carousel-item imageslider">
            <img src="./images/home3.jpg" class="img-fluid" alt="...">
           <p class="para">Project Management</p>
          </div>
        </div>
      </div>
      </div>
      </div>
    <!-- Carousel End -->
    <!-- GUYBrand Limited -->
    <GuyBrandLTD/>
    <!-- GUYBrand Limited End -->
       <!-- <div>
           <FooterView v-bind:url_data="url_data">
           </FooterView>
        </div>-->
  </div>

</template>


<script>
import GuyBrandLTD from './GuyBrandLTD'
//import FooterView from './FooterView'
export default {
  name: 'HomeView',
  components: { 
    GuyBrandLTD,
    //FooterView
  },
  /*mounted(){
     this.url_data=this.$route.name;
    },*/
  data(){
    return{
      //url_data: ""
    }
  },
 
}
</script>

<style scoped>
.imageslider img{
  max-width:100%;
  height:800px;
}
.home{
margin-top:-10px;
padding-top:0px;
}
.move button{
 background-color: orange;
}
.para{ 
  position: absolute;
  text-align: center;
  top: 50%;
  width: 100%;
  font-size:25px;
  font-weight: bold;
  color:black;
}

.img-fluid{
  opacity:0.9;
}
.move{
  margin:auto;
}
@media only screen and (max-width:500px) {
  .smallscreen img{
    max-width: 100%;
  }
}

</style>

