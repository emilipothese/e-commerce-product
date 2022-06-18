<template>
  <section class="menu">
    <nav class="menu__nav--desktop">
      <img src="../assets/logo.svg" alt="">
      <ul class="menu__list">
        <li>Collections</li>
        <li>Men</li>
        <li>Woman</li>
        <li>About</li>
      </ul>
    </nav>

    <nav class="menu__nav--mobile">
      <img src="../assets/icon-menu.svg" alt="">
      <img src="../assets/logo.svg" alt="">
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
    border-bottom: .1rem solid hsl(220, 14%, 75%);
    padding-bottom: 1.5rem;
  }

  .menu__nav--desktop {
    display: flex;
    align-items: center;
  }

  .menu__nav--mobile {
    display: none;
  }

  .menu__list {
    display: flex;
  }

  .menu__list li {
    display: flex;
    padding: 0 20px;
    color: hsl(219, 9%, 45%);
  }

  .menu__profil {
    display: flex;
    align-items: center;
    justify-content: space-around;
  }

  .menu__profil img:nth-child(2){
    width: 40%;
  }

  @media screen and (max-width: 900px) {
    .menu__nav--desktop {
      display: none;
    }

    .menu__nav--mobile {
      display: flex;
      align-items: center;
    }

    .menu__nav--mobile img:nth-child(2) {
      padding-left: 15px;
    }

    .menu__profil img:nth-child(2){
    width: 25%;
  }
  }
</style>
