<template>
  <div class="container">
    <h1 hidden>
      Face It LA
    </h1>
    <logo />
    <div class="tagline">
      Face masks handmade in the city of Los Angeles
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 0 20px;
}

.btn {
  padding: 16px 40px 15px;
  background: red;
  color: white;
  border-radius: 4px;
  font-size: 18px;
  background-image: linear-gradient(90deg, #ff8c00, #f567ea);
  border: 2px solid white;
  font-weight: bold;
  text-decoration: none;
}

.tagline {
  margin: 50px 0 0;
  padding: 0 40px;
  font-size: 0.9rem;
}

@media (min-width: 600px) {
  .tagline {
    display: none;
  }
}
</style>
