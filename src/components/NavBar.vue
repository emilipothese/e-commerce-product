<template>
  <section class="menu">
    <nav class="menu__nav">
      <img src="../assets/logo.svg" alt="">
      <ul class="menu__list">
        <li>Collections</li>
        <li>Men</li>
        <li>Woman</li>
        <li>About</li>
      </ul>
    </nav>

    <div class="menu__profil">
      <img src="../assets/icon-cart.svg" alt="">
      <img src="../assets/image-avatar.png" alt="">
    </div>
  </section>
</template>


<style scoped>
  .menu {
    display: flex;
    justify-content: space-between;
  }

  .menu__nav {
    display: flex;
    align-items: center;
  }

  .menu__list {
    display: flex;
  }

  .menu__list li {
    display: flex;
    padding: 0 20px;
  }

  .menu__profil {
    display: flex;
    align-items: center;
  }

  .menu__profil img{
    width: 60%;
  }
</style>
