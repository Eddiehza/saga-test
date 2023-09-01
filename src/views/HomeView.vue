<script setup lang="ts">
import Header from "@/components/Header.vue"
import HomeMain from "@/components/HomeMain.vue"
import Usercard from "@/components/Usercard.vue"
import { reactive } from "vue";

const userinfo = reactive([
  {
    avatar:"/images/image-emily.jpg",
    opinion:"We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.",
    name:"Emily R.",
    occupation:"Marketing Director"
  },
  {
    avatar:"/images/image-thomas.jpg",
    opinion:"Sunnyside's enthusiasm coupled with their keen interest in our brand's success made it a satisfying and enjoyable experience.",
    name:"Thomas S.",
    occupation:"Chief Operating officer"
  },
  {
    avatar:"/images/image-jennie.jpg",
    opinion:"Incredible end result! Our sales increased over 400% when we worked with Sunnyside.Highly recommended!",
    name:"Jennie F.",
    occupation:"Business Owner"
  }
])
</script>

<template>
  <Header/>
  <HomeMain/>
  <div class="home-users">
    <div class="user-title">CLIENT TESTIMONIALS</div>
    <div class="user-section">
      <Usercard v-for="(item,index) in userinfo" :key="index" :name="userinfo[index].name" :avatar="userinfo[index].avatar" :opinion="userinfo[index].opinion" :occupation="userinfo[index].occupation"/>
    </div>
  </div>
</template>

<style scoped>
.home-users {
  width: 100%;
  height: 780px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.user-title {
  color:#a9a8ad;
  font-size: 17px;
  font-weight: 700;
  letter-spacing: 3px;
}

.user-section {
  margin-top: 20px;
  display: flex;
}
</style>