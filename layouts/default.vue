<template>
  <div :class="classes">
    <header>
      Face masks handmade in the city of Los Angeles
    </header>
    <nuxt />
    <footer>
      <a href="mailto:wearegoingtofaceit@gmail.com" target="_blank">
        email us
      </a>
      <a href="https://www.instagram.com/face.it.la/" target="_blank">
        @face.it.la
      </a>
    </footer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isReady: false
    }
  },
  computed: {
    classes () {
      return [
        'layout',
        { 'is-ready': this.isReady }
      ]
    }
  },
  mounted () {
    setTimeout(() => {
      this.isReady = true
    }, 600)
  }
}
</script>

<style>
html {
  font-family: 'Work Sans', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  color: #fff;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

body {
  background: linear-gradient(-45deg, rgba(150, 157, 255, 0.8), rgba(211, 118, 255, 0.8), rgba(150, 157, 255, 0.8), rgba(211, 118, 255, 0.8));
  background-size: 400% 400%;
  animation: gradient 18s cubic-bezier(0.62, 0.07, 0.35, 1) infinite;
  font-size: 1.06rem;
  letter-spacing: 0.03em;
}

img {
  max-width: 100%;
}

header,
footer {
  position: fixed;
  left: 0;
  width: 100%;
  padding-left: 20px;
  padding-right: 20px;
  text-align: center;
  text-transform: lowercase;
  opacity: 0;
  transform: scale(0.98);
  transition: opacity 1000ms cubic-bezier(0.65, 0.09, 0.43, 0.96), transform 2000ms cubic-bezier(0.44, 0.02, 0.18, 0.9);
}

.layout.is-ready header,
.layout.is-ready footer {
  opacity: 1;
  transform: scale(1);
}

header {
  top: 0;
  padding-top: 20px;
}

@media (max-width: 599px) {
  header {
    display: none;
  }
}

footer {
  bottom: 0;
  padding-bottom: 20px;
}

footer a {
  display: inline-block;
  color: #fff;
  margin: 0 16px;
  text-decoration: none;
  padding-bottom: 3px;
  border-bottom: 2px solid rgba(255, 255, 255, 0.3);
  transition: border-bottom-color 300ms ease-out;
}

footer a:hover,
footer a:focus {
  border-bottom-color: rgba(255, 255, 255, 0.7);
}
</style>
