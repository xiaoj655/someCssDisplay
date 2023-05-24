<template>
<div class="box">
  <h3>CSS</h3>
</div>
</template>

<style scoped>
.box {
  display: flex;
  position: relative;
  width: 180px;
  height: 250px;
  border-radius: 20px;
  background: rgba(0,0,0,0.8);
  color: white;
  /* text-align: center; */
  text-shadow: 2px 2px pink;
  font-size: 4rem;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
h3 {
  z-index: 1;
}
.box::before {
  content: "";
  position: absolute;
  width: 120px;
  height: 120%;
  background: linear-gradient(#0cf,#d500f9);
}
.box::after {
  content: "";
  position: absolute;
  background-color: #0e1538;
  inset: 5px;
  border-radius: 20px;
}
.box::before {
  animation: rotate 4s linear infinite;
}
@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(180deg);
  }
}
</style>
