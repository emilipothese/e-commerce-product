<template>
  <Transition name="modal">
    <div v-if="show" class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-header">
            <slot name="header">default header</slot>
            <button
                class="modal-default-button"
                @click="$emit('close')"
              >OK</button>
          </div>

          <div class="modal-body">
            <slot name="body">
              <div v-if="product.length" class="product">
                <img class="product__image" src="../assets/image-product-1-thumbnail.jpg" alt="">
                <div>
                  <p>Fall limited edition...</p>
                  <p>$125.00</p>
                </div>
              </div>
              <div v-else>
                <p>Your cart is empty.</p>
              </div>
            </slot>
          </div>

          <div class="modal-footer">
            <slot name="footer">
              <button class="cart__btn">Checkout</button>
            </slot>
          </div>
        </div>
      </div>
    </div>
  </Transition>
</template>

<script>
export default {
  props: {
    show: Boolean
  },

  data() {
    return {
      product: {
        1: {
          img: "../assets/image-product-1-thumbnail.jpg",
          title: "Fall limited Edition",
          price: '$125.00'
        }
      }
    }
  },
}
</script>

<style>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 300px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
}

.modal-header {
  display: flex;
  align-content: space-around;
}

.modal-header h3 {
  margin-top: 0;
  padding-bottom: 5px;
  color: black;
  border-bottom: 1px solid hsl(219, 9%, 45%);
}

.modal-default-button {
  margin-left: 10px;
}

.modal-body {
  margin: 20px 0;
}

.product {
  display: flex;
}

.product__image {
  width: 30%;
  margin-right: 15px;
}

.cart__btn {
  background-color: hsl(26, 100%, 55%);
  border-radius: 7px;
  border: hsl(26, 100%, 55%);
  color: white;
  font-weight: 700;
  font-size: 1rem;
  padding: 15px 0;
  width:60%;
}

.cart__btn:hover {
  background-color: hsl(220, 13%, 13%);
  cursor: pointer;
  transition: all .3s ease-out;
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the modal transition by editing
 * these styles.
 */

.modal-enter-from {
  opacity: 0;
}

.modal-leave-to {
  opacity: 0;
}

.modal-enter-from .modal-container,
.modal-leave-to .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>

  <!-- Si il y a quelque chose dans le panier (CartView) -> Affiche le nombre d'items dans le rond orange du cart
      Sinon n'affiche rien

      Créer un array vide par défaut qui est rempli quand le user clique sur Add to cart
      Le CartView reprend le contenu de l'array
      Le CartView ne s'affiche que si click sur cart
  -->
