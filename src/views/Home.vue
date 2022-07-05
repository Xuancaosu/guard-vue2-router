<template>
    <Guard appId="5f6265c67ff6fdae64ec516e" @login="onLogin"></Guard>
</template>

<script>
import { Guard } from '@authing/vue-ui-components'
import "@authing/vue-ui-components/lib/index.min.css";


export default {
  name: 'Home',
  components: {
    Guard
  },
  data() {
    return {
      config: {
        mode: "modal",
      },
      visible: true,
    }
  },
  methods: {
    onLogin() {
      console.log('login')
      this.$router.push('/about')
    }
  },
  beforeUnmount() {
    console.log('beforeUnmount')
  },
  beforeDestroy() {
    console.log('beforeDestroy')
  }
}
</script>
