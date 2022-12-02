<script>

export default {
}
</script>

<template>
  <header id="header">
    <div class="logo">
      <a href="#"><img src="../img/logo.svg" alt="FA EXHIBITION"></a>
    </div>

    <nav id="nav">
      <ul class="menu">
        <li><a href="#">TOP</a></li>
        <li><a href="#information">INFORMATION</a></li>
        <li><a href="#gallery">GALLERY</a></li>
        <li><a href="#access">ACCESS</a></li>
        <li><a href="#contact">CONTACT</a></li>
      </ul>
    </nav>

    <div class="hamburger">
      <span></span>
      <span></span>
      <span></span>
    </div>
  </header>
</template>

<style scoped>
header {
  background-color: #050507;
  color: #fff;
  margin: 0;
}
li a {
  color: #fff;
}
ul {
  list-style: none;
}
.logo {
  line-height: 1px;
  position: fixed;
  top: 35px;
  left: 30px;
  /* 一番上にくるように設定 */
  z-index: 40;
  /* display: none; */
}
.logo a {
  display: block;
}

.menu {
  padding: 0;
}

</style>
