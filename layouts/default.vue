<template>
  <div>
      <Nuxt />
      <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue';

export default {
	components: {
		Footer
	}
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
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

body {
  background-color: #212121;

  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 100%;
  text-align: center;
  margin: 10% 0;
  min-height: 200px;
  align-items: center;
  
  border: 1px solid #fff;
}

.title {
  font-size: xx-large;
  color: #E55E5B;
  margin-bottom: 0;

  border: 1px solid #fff;
}

.title p {
  font-size: large;
  color: white;
  margin-top: 0;

  border: 1px solid #fff;
}

.button {
  padding: 10px 20px;
  border-radius: 5px;
  border: 1px solid white;
  border-radius: 5px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all .2s;
  background-color: #E55E5B;
  color:white;
  font-weight: 500;
  text-decoration: none;
  font-size: x-large;

  flex: 1 auto;
  justify-content: space-around;
}

.button:hover {
  padding: 15px 25px;
  color: #E55E5B;
  background-color: white;
  border: 1px solid #E55E5B;
}
</style>