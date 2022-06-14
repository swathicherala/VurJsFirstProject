<template>
<div class="main1">
  <div class="container">
      <div class="row justify-content-evenly align-items-center">
        <div class="col-sm-4 shift text-center pb-4" style="margin-top:20px;">
          <div>
              <img src="./images/logo.svg" class="image2">
          </div>
         <!-- <ul class="listing">

             <li>
                  <router-link to="/" id="hidehome" @click="HideHome()" v-show="visible=false">Home</router-link>
              </li>
              <li>
                  <router-link to="/" id="hidehome" @click="HideHome()" v-show="visible=false">Home</router-link>
               
              </li>
              <li>
                  <router-link to="/about" id="hideabout" @click="HideAbout()">About</router-link>
              </li>
              <li>
                  <router-link to="/services" id="hideservices" @click="HideServices()">Services</router-link>
              </li>
              <li>
                  <router-link to="/contact" id="hidecontact" @click="HideContact()">Contact</router-link>
              </li> 
              <li>
                  <router-link :to="item.link" :v-for="item in items" 
                  :key="item.name"
                  id="hidecontact" > {{item.name}}</router-link>
              </li>
          </ul>-->
          <!--router-->
           <!--<router-link
            v-for="item in items"
            :key="item.name"
            class="nav-link data-link"
            id="datalink"
            :to="item.link"
            @click="HidePage(item.name)"
            @click.native="scrollToTop">
            {{ item.name }}</router-link>
            current location:{{url_data}}-->
          <!--router end-->
          <div v-for="(nav, index) in items" :key="index"
          @click.native="scrollToTop" class="hide">
            <span v-show="nav.name !== this.$route.name" 
            @click="changeRoute(nav, index)">{{ nav.name }}</span>
          </div>
        </div>

        <div class="col-sm-4 foot2" v-show="this.$route.name !== 'Contact'">
            <h1 class="heading">
                Get in touch
                <hr/>
            </h1>
            <div class="address">
                <p class="texts">
                Please feel free to get in touch with us regarding any of our services using the following details
            </p>
            <ul class="footerlist">
                <li>
                   Office 973,<br/>
                   58 Peregrine Road,<br/>
                   Ilford IG6 3SZ
                </li>
                <li>
                    Phone: 0207 183 0754
                </li>
                <li>
                    Email: <a href="" style="text-decoration:none;">sales@guybrand.co.uk</a>
                </li>
            </ul>
            </div>
        </div>

        <div class="col-sm-4" v-show="this.$route.name !== 'Contact'">
            <h1 class="heading">
                Where we are
            </h1>
            <hr />
            <div class="location">
                <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d9910.678011269529!2d0.125367!3d51.61094400000001!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47d8a391bf87eca5%3A0xab394731bb9cc927!2s973%2C%2058%20Peregrine%20Rd%2C%20Ilford%20IG6%203SZ%2C%20UK!5e0!3m2!1sen!2sin!4v1654517510622!5m2!1sen!2sin" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"  class="map">
                </iframe>
            </div>
        </div>
    </div>
  </div>
</div>
</template>

<script>
//import { RouterLink } from 'vue-router';
//import index from '../router';
export default{
    name:'FooterView',
    components:{
        //index
    },
     
    data(){
        return{
       items: [
        {
          link: "/",
          name: "Home",
        },
        {
          link: "/about",
          name: "About",
        },
        {
          link: "/services",
          name: "Services",
        },
        {
          link: "/contact",
          name: "Contact",
        },
      ]
     }   
    },
  props:{
        url_data:{
            type:String,
        }
    },  
  methods:{
      changeRoute(data, index) {
      console.log("data", data, index);
      const newArray = this.items
      console.log(data.name)
      this.$router.push(data.link)
    },
      /*HidePage(val){
         // console.log(this.url_data)
          //console.log(this.$data.items.name)
          console.log(val)
            let v=val;
             console.log(v);
                //console.log(this.items.name);
          if(v==v){
              //console.log(this.url_data)
                const home=document.getElementById("datalink").style.display = "none";
                //console.log(this.url_data)
               console.log("Hi");
            }
            else{
                console.log("Ohh Noooo")
            }
            
            /*for (let str of this.items) {  
               console.log(str.name); 
               if(this.url_data==str.name){
              //console.log(this.url_data)
               
                //console.log(this.url_data)
            }
            } 
      },*/
      scrollToTop() {
          window.scrollTo(0,0);
      }
  }
    /*methods:{
        HideHome(){
            const home=document.getElementById("hidehome").style.display = 'none';
            const home1=document.getElementById("hideabout").style.display = 'block';
            const home2=document.getElementById("hideservices").style.display = 'block';
            const home3=document.getElementById("hidecontact").style.display = 'block';
            //let container = this.$refs.home
            //console.log(this.$router.currentRoute.path );
            //console.log(this.$router.name);
        },
        HideAbout(){
            const about=document.getElementById("hideabout").style.display = 'none';
            const about1=document.getElementById("hidehome").style.display = 'block';
            const about2=document.getElementById("hideservices").style.display = 'block';
            const about3=document.getElementById("hidecontact").style.display = 'block';
        },
        HideServices(){
            const services=document.getElementById("hideabout").style.display = 'block';
            const services1=document.getElementById("hidehome").style.display = 'block';
            const services2=document.getElementById("hideservices").style.display = 'none';
            const services3=document.getElementById("hidecontact").style.display = 'block';
        },
         HideContact(){
            const contact=document.getElementById("hideabout").style.display = 'block';
            const contact1=document.getElementById("hidehome").style.display = 'block';
            const contact2=document.getElementById("hideservices").style.display = 'block';
            const contact3=document.getElementById("hidecontact").style.display = 'none';
        }
    }*/
}
</script>

<style scoped>
.main1{
    background-color:rgb(190, 187, 187);
}
.hide{
    color:#2f7ef5;
    padding-left:40px;
    font-weight: bold;
    font-size:20px;
    cursor: pointer;
}
.align-items-center{
   justify-content: space-evenly;

    align-items: center;
}
.heading{
    color:#2f7ef5;
    font-size:25px;
    text-align: left;
    padding-top:20px;
    cursor:pointer;
}
.texts{
    text-indent: 0px;
}
.listing li{
list-style:none;
padding:3px;
font-size: 12px;
margin-right:12px;
}
.listing{
    margin-top:-15px;
    padding-right:10px;
}
.listing li a{
    text-decoration: none;
    font-size: 20px;
}
hr{
    background-color:blue;
}
.map{
    width:200px;
    height:150px;
}
.footerlist li{
    text-align: left;
    font-size: 12px;
    font-weight: bold;
}
.image2{
    margin-top:-14px;
    width:100%;
    height:100px;
    padding-left:55px;
}

@media only screen and (max-width:500px){
.texts .footerlist{
    text-align: center;
}
.foot2{
    justify-content: center;
}
.texts{
    text-indent: 14px;
}
.heading{
    text-align: center;
}
.footerlist{
    width: 30%;
    margin:auto;
    padding-bottom: 20px;
}
.shift{
    text-align:center;
}
.location{
    text-align: center;
}
}

</style>