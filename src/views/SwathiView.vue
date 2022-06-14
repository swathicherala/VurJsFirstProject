<template>
  <footer>
    <div class="container grey-footer">
      <div class="row justify-content-evenly align-items-center footer">
        <div
          class="nav footer-column-1 flex-column col-sm-12 col-md-4 text-center"
        >
          <router-link class="nav-link active" aria-current="page" to="/">
            <img
              src="../assets/images/logo.svg"
              style="width: 40%"
              class="img-fluid"
              alt=""
            />
          </router-link>
          <!-- <router-link class="nav-link datalink" v-if="!task.isCompleted" to="/"
            >Home</router-link
          >
        </div> -->
          <!--
          <router-link
            v-for="(data, index) in navigation"
            @click="change(index)"
            :v-if="routedata == data.name"
            :key="data.name"
            class="nav-link data-link"
            id="datalink"
            :to="data.link"
            >{{ data.name }}{{ routedata }}</router-link
          > -->
          <router-link
            class="nav-link datalink"
            v-if="home"
            @click="change('Home')"
            to="/"
            >Home</router-link
          >
          <router-link
            class="nav-link datalink"
            v-if="about"
            @click="change('About')"
            to="/about"
            >About</router-link
          >
          <router-link
            class="nav-link datalink"
            v-if="service"
            @click="change('Service')"
            to="/services"
            >Services</router-link
          >
          <router-link
            class="nav-link datalink"
            v-if="contact"
            @click="change('Contact')"
            to="/contact"
            >Contact</router-link
          >
        </div>
        <div class="col-sm-12 col-md-4">
          <div class="padd">
            <div class="footer-heading">
              <h3 class="titlefoot">Get in touch</h3>
              <hr class="home-line" />
              <p class="footer-data">
                Please feel free to get in touch with us regarding any of our
                services using the following details
              </p>
              <div class="footer-list">
                <ul>
                  <li>
                    Office 973,
                    <br />
                    58 Peregrine Road,
                    <br />
                    Ilford IG6 3SZ
                  </li>
                  <li>Phone: <a class="num" href="">0207 183 0754</a></li>
                  <li>
                    Email:
                    <a class="num">sales@guybrand.co.uk</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        <div class="col-sm-12 col-md-4">
          <div class="padd">
            <div class="footer-heading">
              <h3 class="titlefoot">Where we are</h3>
              <hr class="home-line" />
              <Map />
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
import Map from "./Map.vue";
export default {
  name: "Footer",
  data() {
    return {
      routedata: "",
      // HideHome: false,
      // console.log(router);
      // navigation:""
      home: true,
      about: true,
      service: true,
      contact: true,
      navigation: [
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
          name: "Service",
        },
        {
          link: "/contact",
          name: "Contact",
        },
      ],
    };
  },
  created() {
    console.log("current route", this.$route.query.page);
  },
  methods: {
    // console.log(router);
    change(Value) {
      // console.log(Value);
      this.home = false;
      this.about = true;
      this.service = true;
      this.contact = true;
      if (Value == "Home") {
        this.home = false;
        this.about = true;
        this.service = true;
        this.contact = true;
      }
      if (Value == "About") {
        this.about = false;
        this.home = true;
        this.service = true;
        this.contact = true;
      }
      if (Value == "Service") {
        this.service = false;
        this.about = true;
        this.home = true;
        this.contact = true;
      }
      if (Value == "Contact") {
        this.contact = false;
        this.service = true;
        this.about = true;
        this.home = true;
      }
      // console.log(this.$router.currentRoute._value.name + " value");
    // console.log("current func", this.$route);
    // console.log("current func", this.$router);
      // this.navigation.splice(id, 1);
      // console.log(this.$route);
      // console.log(this.$route.name);
      // console.log(this);
      // console.log(this.$route.path);
      // this.routedata = this.$router.currentRoute._value.name;
      // console.log(this.routedata);
      // if (this.routedata != this.navigation.name) {
      //   document.getElementById("datalink").style.display = "none";
      //   document.getElementById("datalink").remove;
      //   // this.navigation.name;
      // }
      // this.routedata = false;
      // let abc = document.querySelector(".datalink");
      // console.log(abc);
      // let vicky = abc.map(function (val) {
      //   return val;
      // });
      // console.log(vicky);
    },
  },
  components: {
    Map,
  },
};
</script>
<style scoped>
.num {
  /* font-weight: 400; */
  text-decoration: none;
  color: #000;
  cursor: pointer;
}
.num:hover {
  color: rgb(0, 51, 102) !important;
}
.footer {
  background-color: #B8BAB9 !important;
}
.grey-footer {
  max-width: 100% !important;
  background-color: #B8BAB9 !important;
  color: #fff;
  font-weight: 800px;
  line-height: 28px;
  font-size: 18px;
  padding-top: 2% !important;
  padding-bottom: 2% !important;
}
.justify-content-evenly {
  justify-content: space-evenly;
}
.align-items-center {
  align-items: center;
}
.footer-column-1 {
  text-align: center;
  font-size: 20px;
  padding-bottom: 4%;
}
.nav-link {
  color: #0D6EFD;
}
.active,
.nav-link:hover {
  color: #2F7EF5 !important;
}
.titlefoot {
  color: #2F7EF5 !important;
}
.home-line {
  background: #2F7EF5;
  height: 1px;
  margin: 1rem 0;
  color: inherit;
  border: 0;
  /* opacity: 0.25; */
}
/* .home-line:not([size]) {
  height: 1px;
} */
.footer-data {
  font-size: 16px;
  line-height: 1;
  color: #2F7EF5 !important;
  padding-bottom: 20px;
}
.footer-heading {
  padding: 0 40px;
}
.footer-list {
  color: #000;
}
@media only screen and (max-width: 766px) {
  .padd {
    margin-right: 10%;
    margin-left: 10%;
  }
  .titlefoot {
    text-align: center;
  }
}
@media only screen and (max-width: 350px) {
  .footer-data {
    font-size: 12px;
  }
}
@media only screen and (max-width: 450px) {
  .footer-data {
    font-size: 13px;
  }
}
@media only screen and (max-width: 576px) {
  .footer-list ul {
    padding: 0;
    font-size: 15px;
  }
  .footer-heading {
    padding: 0;
  }
}
</style>