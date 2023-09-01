<script setup lang="ts">
const props = defineProps(["avatar","opinion","name","occupation"])
</script>

<template>
  <div class="user-card">
    <div class="user-avatar" :style="{ backgroundImage: 'url(' + props.avatar + ')' }"></div>
    <div class="user-opinion">{{ props.opinion }}</div>
    <div class="user-name">{{ props.name }}</div>
    <div class="user-occupation">{{ props.occupation }}</div>
  </div>
</template>


<style scoped>
.user-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 415px;
  width: 340px;
  padding: 15px;
  cursor: pointer;
  border-radius: 20px;
  transition: box-shadow 0.4s;
}

.user-card:hover {
  box-shadow:
  2.8px 2.8px 2.2px rgba(0, 0, 0, 0.011),
  6.7px 6.7px 5.3px rgba(0, 0, 0, 0.016),
  12.5px 12.5px 10px rgba(0, 0, 0, 0.02),
  22.3px 22.3px 17.9px rgba(0, 0, 0, 0.024),
  41.8px 41.8px 33.4px rgba(0, 0, 0, 0.029),
  100px 100px 80px rgba(0, 0, 0, 0.04)
  ;
}

.user-avatar {
  border-radius: 9999px;
  width: 72px;
  height: 72px;
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
}

.user-opinion {
  margin-top: 80px;
}

.user-name {
  margin-top: 75px;
  color: #293740;
  font-weight: 800;
}

.user-occupation {
  margin-top: 10px;
  color: #c2c1bf;
}

.user-card > div {
  display: flex;
  text-align: center;
}
</style>