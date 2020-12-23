<template>
  <div class="home">
    <Drawer></Drawer>
  </div>
</template>

<script>
// @ is an alias to /src
import Drawer from '@/components/Drawer.vue'

export default {
  name: 'home',
  components: {
    Drawer
  }
}
</script>
