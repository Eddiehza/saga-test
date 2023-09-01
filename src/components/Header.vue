<script setup lang="ts">

</script>

<template>
  <div class="header-all">
    <img class="header-logo" src="/images/logo.svg" alt="">
    <div class="header-menu">
      <div class="choices">About</div>
      <div class="choices">Services</div>
      <div class="choices">Projects</div>
      <div class="choices contact">CONTACT</div>
    </div>
  </div>
</template>


<style scoped>
.header-all {
  width: 100%;
  height: 120px;
  background-color: rgba(0, 0, 0, 0);
  position: fixed;
  display: flex;
  align-items: center;
}

.header-logo {
  height: 35px;
  margin-left: 40px;
}

.header-menu {
  height: 100%;
  display: flex;
  align-items: center;
  gap: 5px;
  margin-left: auto;
  margin-right: 40px;
}

.choices {
  padding: 20px;
  color: white;
  font-size: 20px;
  cursor: pointer;
  border-radius: 30px;
  transition: background-color 0.2s;
}

.choices:hover {
  background-color: rgba(255, 255, 255, 0.221);
}

.contact {
  padding: 15px;
}
</style>