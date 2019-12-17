<template>
  <div>
    <div class="container-fluid">
      <header class="py-4 py-sm-5">
         <!-- <b-navbar class="p-0" toggleable="lg" type="light">
            <b-navbar-brand>
              <b-navbar-brand class="font-family-headings" to="/">
                <span class="h3 text-dark">Oskar Laurin</span>
              </b-navbar-brand>
            </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
              <b-navbar-nav class="ml-auto ">
                <b-nav-item to="/" exact-active-class="active">Home</b-nav-item>
                <b-nav-item to="/about" active-class="active">About</b-nav-item>
              </b-navbar-nav>
            </b-collapse>
        </b-navbar> -->

      <div class="row">
      <div class="col-10">
        
         <h2>
          Oskar Laurin is a Stockholm based designer, 
          working in the fields of visual communication and art direction.
          </h2>
          <h2>MFA in Visual Communication from Konstfack.</h2> 
        
        <h2>laurin.oskar@gmail.com</h2>
        
      </div>
    </div>
        
      </header>
      <b-row class="align-items-start">
        <transition name="fade" appear>
          <b-col tag="main" cols="12" class="bg-white p-0 rounded shadow-lg">
            <div class="overflow-hidden p-4 p-sm-5 ">
              <slot/>
            </div>
          </b-col>
        </transition>
        <!-- <site-sidebar/> -->
      </b-row>
      <site-footer/>
    </div>
  </div>
</template>


<script>
// import SiteSidebar from '~/components/SiteSidebar.vue'
import SiteFooter from '~/components/SiteFooter.vue'
import Swiper from "swiper"

export default {
  
  components: {
    // SiteSidebar,
    SiteFooter
  },
  mounted() {
  var mySwiper = new Swiper ('.swiper-container', {
    // Optional parameters
    direction: 'horizontal',
    loop: true,

    // If we need pagination
    pagination: {
      el: '.swiper-pagination',
    },

    // Navigation arrows
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev',
    },

    // And if we need scrollbar
    scrollbar: {
      el: '.swiper-scrollbar',
    },
  })
  }
}

</script>

<style>
.fade-enter-active {
  transition: .5s;
}

.fade-enter {
  opacity: 0;
}
</style>