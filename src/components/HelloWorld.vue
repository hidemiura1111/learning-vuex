<template>
  <div>
    <button @click="incrementAction">+</button>
    <button @click="addCount">+10</button>

  </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'HelloWorld',
  props: {
  },
  methods: {
    // Call actions by mapActions
    ...mapActions(['incrementAction', 'addCountAction']),
    addCount() {
      this.addCountAction({
        value: 10
      })
    }

    // Call mutations
    // increment() {
    //   this.$store.commit('increment')
    // },
    // addCount() {
    //   this.$store.commit('addCount', {
    //     value: 10
    //   })
    // }

    // Call actions
    // increment() {
    //   this.$store.dispatch('incrementAction')
    // },
    // addCount() {
    //   this.$store.dispatch('addCountAction', {
    //     value: 10
    //   })
    // }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
