<template>
  <div>
    <nuxt />
  </div>
</template>

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

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

html {
  scroll-behavior: smooth;
}

.banner {
        height: 450px;
        width: 100%;
        object-fit: cover;
        object-position: top center;
        filter: grayscale();
    }

:root {
  --highlight-one: #ce922a
}

* {
  box-sizing: border-box;
}

body {
  background-color: #f6faf9;
}

.flex {
  display: flex;
}

@media only screen and (max-width: 420px) {
  .container {
    padding: 20px;
  }

  .banner {
    height: 250px;
    filter: grayscale();
  }

}

@media only screen and (min-width: 421px) {
  .container {
    width: 1000px;
    margin:auto;
  }

}

</style>
