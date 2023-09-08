<template>
  <vue-app id="home">
      <NavBar />
    <v-container fluid>
        <div class="head">
          <v-row>
            <v-col cols="5">
              <div style="position: relative" class="mt-16">
                <h1 class="text-grey">hi world,</h1>
                <h1 class="text-White">I'm Camilo Rendon</h1>
                <span class="text-grey">web Developer</span><br/>
                <v-btn title dark class="text-yellow mt-8" variant="outlined">Contact me</v-btn>
              </div>
            </v-col>
            <v-col cols="2">
              <div style="position: absolute; z-index:9999;bottom:0;margin-left:auto;margin-right:auto;left:0;right:0;text-align:center">
                <v-icon>fas fa-angle-double-down</v-icon>
              </div>
            </v-col>
            <v-col cols="5">
              <div style="position: relative;z-index: 9999;" class="mt-5">
                <v-img src="fotoyo-origin.png" contain max-height="300"></v-img>
              </div>
            </v-col>
          </v-row>
        </div>
        <v-col cols="12" class="mt-16" id="about">
          <div>
            <v-row>
              <v-col cols="12" sm="6">
                <div class="egg">
                  <v-img src="i2.png" max-height="300"></v-img>
                </div>
              </v-col>
              <v-col cols="12" sm="6">
                <h5 class="mt-16"> About Me</h5>
                <div style="width:120px">
                  <v-slider v-model="slider2" color="yellow">

                  </v-slider>
                </div>
                <h4 class="mt-4">I am a Creative Web Design</h4>
                <h4>And Developer</h4>
                <p class="text-grey">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Illum maxime a libero ipsa accusantium necessitatibus est delectus velit sequi facere deleniti laborum nisi ratione eveniet, cumque 
                  laudantium assumenda ullam in!

                </p>
              <br/>  
              <p class="text-grey">Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
                Exercitationem consequuntur tempora quia ullam quaerat, ipsam, quae ea laudantium 
                iusto aspernatur architecto saepe aliquam blanditiis sunt quisquam voluptatibus tenetur. Eius, id.
              </p>
              <v-btn title dark color="yellow" class="mt-4">
                Download Resume
              </v-btn>
              </v-col>
            </v-row>
          </div>
        </v-col>
        <div class="text-center mt-4">
          <h2>What we Do</h2>
          <div style="width: 120px; margin: 0 auto">
            <v-slider v-model="slider2" color="yellow"></v-slider>
          </div>
        </div>
    </v-container>
  </vue-app>
</template>

<script>
import {defineComponent} from 'vue';
import NavBar from '@/components/NavBar.vue'

export default defineComponent({
    name: 'HomeView',
    setup(){
      return{
        slider2:50,

        items: [
        {
          img: "i3.jpg",
        },
        {
          img: "i4.jpg",
        },
        {
          img: "i5.jpg",
        },
        {
          img: "i6.jpeg",
        },
        {
          img: "i9.jpg",
        },
        {
          img: "i8.jpg",
        },
      ],
      }
    },

    components: {
        NavBar,
    },
})
</script>

<style scoped>
.v-container{
  padding: 16px 0;
}
.head{
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before{
  content: " ";
  position: absolute;
  top: 0px;
  left: 0px;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg );
}
.head:after{
  content: " ";
  position: absolute;
  top: 0px;
  right: 0px;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}
.egg{
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #FBDF7E;
  border-radius: 60% 60% 40% 60% /60% 60% 40% 80%;

}
</style>