<template>
  <div>
    <svgIcons/>
    <asideBase/>
    <headerBase/>
    <breadcrumbs/>
    <nuxt/>
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

  .container {
    max-width: 1020px;
    width: 100%;
    margin: 0 auto;
  }

  .content {
    margin-left: 176px;
  }

  .d-fc {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  a {
    text-decoration: none;
  }

  .title {
    font-size: 16px;
    font-weight: bold;
    color: #aeaeae;
    padding-top: 35px;
    margin-bottom: 15px;
  }

</style>
<script>
    import asideBase from "../components/aside";
    import headerBase from "../components/header";
    import svgIcons from "../components/svgIcons";
    import breadcrumbs from "../components/breadcrumbs";

    export default {
        components: {breadcrumbs, headerBase, asideBase, svgIcons}
    }
</script>
