<template>
  <ul>
    <li v-for="prod in cartItems" :key="prod.id">
      <CartItem v-bind:prod="prod" @valChange="valChange" />
    </li>
  </ul>
</template>

<script>
import CartItem from '../components/CartItem.vue'
export default {
  name: 'CartList',
  components: {
    CartItem
  },
  computed: {
    cartItems() {
      return this.$store.state.cart.cart
    }
  },
  methods: {
    valChange: function() {
      this.$emit('valChange')
    }
  }
}
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  width: 100%;
  padding: 1rem 0rem;
}
</style>
