<template>
  <header class="Header" :class="{ fixed: isFixed }">
    <figure>
      <img :src="logo" alt="Logo">
    </figure>
    <a class="btn" href="http://">buy bunzo</a>
  </header>
</template>

<script>
export default {
  props: ["logo", "isFixed"]
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 7%;
  width: 100%;
  position: absolute;
  z-index: 2;
}

header.fixed {
  position: fixed;
  background-color: #fff;
  box-shadow: 2px 0 2px #cecccc;
  z-index: 1;
}

figure {
  cursor: pointer;
}

header.fixed a.btn {
  border-color: #5138EE;
  color: #5138EE;
}
</style>
