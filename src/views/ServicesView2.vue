<template>
  <div class="main">
    <div class="container">
      <div class="row">
      <div class="col-md-6 mt-5">
          <h1 class="text">
              BESPOKE BUILD
          </h1>
        <p class="info">
           If you already have your building concept, architectural drawings and planning permission, you need a trustworthy building company that offers great service and value to turn your plans into reality. We have a vast experience of all sizes of projects and a specialist, all-trades in-house team. One of the best ways of creating your dream home and maximising its value is to find a property and renovate it to suit your individual needs. Many of our renovations involve taking the house back to its shell and completely remodelling.
        </p>
      </div>
      <div class="col-sm-6  mt-5 aboutimage">
       <img src="./images/services1.jpg" class="img-fluid images1">
      </div>
    </div>

     <div class="row mt-5 reverse">
      <div class="col-md-6">
          <h1 class="text">
              DESIGN, PLANNING & BUILDING
          </h1>
        <p class="info">
         If you are at the beginning of your development journey we offer an end-to-end, stress-free package, which includes design, planning and build. The Guybrand Limited specialist team will come up with a variety of inspirational, functional and practical concepts to suit your budget and needs. Our architects know how to balance an exciting vision with practical strategies and legal implications and our large team of skilled builders will turn your plans into reality.
        </p>
      </div>
      <div class="col-sm-6 mb-5 aboutimage">
       <img src="./images/services2.jpg" class="img-fluid images1">
      </div>
    </div>
    </div>
  </div>
</template>

<style scoped>
.text{
    font-size:20px;
    color:orange;
    font-family: Copperplate,Copperplate Gothic Light,fantasy;
    font-weight: bold;
   text-align: center;
   margin-top:60px;
}
.images1{
  width:550px;
  height:400px;
}
.reverse{
  display: flex;
  flex-direction: row-reverse;
}
.images1{
  margin:auto;
  max-width:120%;
}
@media only screen and (max-width:700px){
.img-fluid{
  max-width: 500px;
}

}
@media only screen and (max-width:900px){
.img-fluid{
  max-width: 500px;
}
.img-fluid{
  max-width: 100%;
}
.info{
  font-size: 15px;
}
.text{
  margin-top: -22px;
  }
}
</style>