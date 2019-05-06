<template>
  <div id="app">
    <header class="header">
      <div class="header-text">
        <h1>FarnsCo makes</h1>
        <h2 class="services">Websites</h2>
      </div>
    </header>
    <nav class="nav">
      <g-link class="nav__link" to="/">Home</g-link>
      <g-link class="nav__link" to="/about">About</g-link>
      <g-link class="nav__link" to="/credits">Credits</g-link>
    </nav>
    <div class="layout">
      <slot/>
    </div>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style lang="scss">
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  height: 480px;
  background-image: url("../assets/dorelys-smits-200737-unsplash.jpg");
  background-size: cover;
  .header-text {
    padding: 200px;
    h1,
    h2 {
      color: white;
    }
  }
}

.nav__link {
  margin-left: 20px;
}
</style>
