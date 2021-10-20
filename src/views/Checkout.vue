<template>
    <main class="wrapper">
        <h1> Checkout Page </h1>

        <div>

            <Summary
            :cart="cart"
            :remove="removeItem"
            />

        </div>
    </main>
</template>

<script>
import Summary from '@/components/Summary.vue'

export default {
  components: {
    Summary
  },
  data () {
    return {
      cart: {}
    }
  },
  methods: {
    removeItem (name) {
      delete this.cart[name]
    }
  }
}
</script>
