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
      <a id="show-cart" @click="showCart = true"><img src="../assets/icon-cart.svg" alt=""><span class="number--small">0</span></a>
      <a href="#"><img src="../assets/image-avatar.png" alt=""></a>
    </div>
  </section>

  <Teleport to="body">
    <!-- use the modal component, pass in the prop -->
    <cart-view :show="showCart" @close="showCart = false">
      <template #header>
        <h3>custom header</h3>
      </template>
    </cart-view>
  </Teleport>

</template>

<script>
import CartView from './CartView.vue'

export default {
  components: {
    CartView
  },
  data() {
    return {
      showCart: false
    }
  },
}
</script>

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

  .menu__profil a {
    text-decoration: none;
  }

  .menu__profil a:nth-child(2) img{
    width: 40%;
    border: 2px solid transparent;
    border-radius: 50%;
    transition: all .3s ease-out;
  }

  .menu__profil a:nth-child(2) img:hover{
    border: 2px solid hsl(26, 100%, 55%);
    border-radius: 50%;
  }

  .menu__profil a:nth-child(1) {
    position: relative;
  }

  .number--small {
    font-size: 0.7rem;
    font-weight: 700;
    color: white;
    background-color: hsl(26, 100%, 55%);
    border-radius: 50%;
    padding: 0px 7px;
    position: absolute;
    top: -10px;
    right: -10px;
  }

  @media screen and (max-width: 900px) {
    .menu {
      border-bottom: 0rem;
    }

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
