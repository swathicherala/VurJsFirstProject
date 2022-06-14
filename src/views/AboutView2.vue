<template>
  <div class="main">
    <div class="container">
      <h1 class="texts">
      Why Choose Guybrand Limited?
      </h1>
      <hr style="background-color:blue"/>
      <p class="info">
          Guybrand Limited is a family-run company that has grown organically into a large professional team of skilled tradesmen. We maintain the highest quality of work by only using our own team and partnering with leading architectural, surveyor, design and engineering companies.
      </p><br />
      <p class="info">
          Most of our work comes through customer and professional referrals. This is due to a combination of making sure we truly understand clients’ needs, whilst providing the finest finish through attention to detail and quality workmanship. Every project is personally managed by our directors who collaborate with all parties involved to ensure progress is being made until successful and timely completion.
      </p><br />
      <div class="row">
          <div class="col-md-4">
              <div class="card">
              <div class="card-body box">
              <h4 class="card-title">Quality</h4><hr/>
              <p class="card-text"> We understand any building development is a huge financial investment for you. That’s why we have strict quality controls in place, which allows our experienced team of professionals to deliver top quality results that will increase property value. </p>
              </div>
              </div>
          </div>
         <div class="col-md-4">
              <div class="card">
              <div class="card-body box">
              <h4 class="card-title">Costs</h4><hr/>
              <p class="card-text">  We provide clear detailed quotations that allow you to make informed decisions. Our efficient resource management, build management and innovative building techniques and technology enable us to pass savings on to clients. And this means we are competitive on price.  </p>
              </div>
              </div>
          </div>
         <div class="col-md-4">
              <div class="card">
              <div class="card-body box">
              <h4 class="card-title">TIME</h4><hr/>
              <p class="card-text">  Any building work can be stressful for busy people – especially when you are juggling work and family commitments. Project continuity is vital. Effective project management combined with our committed, all-trades team allows us to deliver – fast!  </p>
              </div>
              </div>
          </div>
      </div>

      <div class="row mt-5">
      <div class="col-md-6">
        <p class="text2">
           Guybrand Limited is fully insured for all our work. We provide defects and structural guarantee on all new installations. And we’ll also sort the paperwork – you’ll get full Building Control approval and other necessary completion certificates. We use only industry standard contracts, with no hidden surprises. We make sure that you have clarity and confidence in what you will receive from Guybrand Limited.
        </p>
      </div>
      <div class="col-sm-6 aboutimage">
       <img src="./images/about1.jpg" class="img-fluid">
      </div>
    </div>

     <div class="row mt-5 reverse">
        <div class="col-md-6">
        <p class="text2">
          Guybrand Limited shares years’ experience in the building industry, construction management and trade qualifications. Over the years they have gained significant experience working for leading construction and blue chip companies. Today Guybrand Limited is stronger than ever thanks to its vision of providing high quality workmanship combined with outstanding personal service and care.
        </p>
      </div>
      <div class="col-sm-6 aboutimage pb-4">
       <img src="./images/about2.jpg" class="img-fluid">
      </div>    
    </div>
  </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.main{
    background-image: url('./images/background.jpg');
}
.texts{
    font-size:25px;
    color:orange;
    font-family: Copperplate,Copperplate Gothic Light,fantasy;
    font-weight: bold;
   text-align: center;
   padding:29px;
}
.info{
  color:white;
  font-size:20px;
}
hr{
  background: grey;
}
.box{
  background: #0d6efd;
  opacity:0.9;
  color:white;
  height:200px;
}
.card-title{
  color:orange;
}
.card-text{
  text-indent: 0;
  font-size:12px;
}
.picture{
  width:350px;
  height:300px;
}
.reverse{
  display: flex;
  flex-direction: row-reverse;
}
@media only screen and (max-width:500px){
.main{
  width:615px;
}
.card{
  width:420px;
  height:250px;
  margin:auto;
  margin-bottom: 15px;
}
}
@media only screen and (max-width:700px){
.main{
  max-width:100%;
}
.card{
  max-width:100%;
  height:250px;
  margin:auto;
  margin-bottom: 15px;
}
.img-fluid{
    margin: 0px;
    width: 204%;
}
.text2{
  margin-top:20px;
}
}
@media only screen and (max-width:900px){
.main{
  width:900px;
}
.card{
  width:219px;
  height:250px;
  margin:auto;
  margin-bottom: 15px;
}
.aboutimage{
  margin:auto;
}
}
</style>