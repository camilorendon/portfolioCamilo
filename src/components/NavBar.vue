<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn>
        <v-icon color="yellow" left class="mr-2">
             fas fa-signature</v-icon>juan
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-yellow">home</v-btn>
    <v-btn text @click="scroll('about')">about</v-btn>
    <v-btn text @click="scroll('portfolio')">portfolio</v-btn>
    <v-btn text @click="scroll('services')">services</v-btn>
    <v-btn text @click="scroll('page')">page</v-btn>
    <v-btn text @click="scroll('biog')">biog</v-btn>
    <v-btn text @click="scroll('contact')">contact</v-btn>
  </v-app-bar>
</template>

<script>
export default {
    mothods: {
        scroll(refName){
            const element = document.getElementById(refName)
            element.scrollIntoView({behavior: "smooth"})
        }
    }
}
</script>

<style>

</style>