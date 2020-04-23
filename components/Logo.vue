<template>
  <div class="logo">
    <img src="~/assets/logo.png"></img>
  </div>
</template>
<style>
.logo {
  width: 100%;
  width: 85vw;
  max-width: 700px;
  margin: 0 auto;
  animation: 2s appear;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
