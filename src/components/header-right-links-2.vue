<template>
  <div>
    <!-- hamburger menu -->
    <a href="#" class="hamburger-menu" @click.prevent="openMenu">
      <inline-svg :src="require('../images/hamburger.svg')"></inline-svg>
    </a>
    <!-- contact us -->
    <contact></contact>
  </div>
</template>

<script>
import contact from './contact.vue'
export default {
  components: {
    contact
  },

  methods: {
    openMenu () {
      Event.$emit('menu-opened')
    }
  }
}
</script>
