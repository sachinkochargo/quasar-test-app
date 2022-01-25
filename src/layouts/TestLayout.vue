<template>
    <GOHeader>
      <router-view />
    </GOHeader>
</template>

<script>
import { GOHeader } from 'go-component-library';

export default {
  name: 'TestLayout',
  props: {
    title: {
      type: String,
      required: true
    },

    caption: {
      type: String,
      default: ''
    },

    link: {
      type: String,
      default: '#'
    },

    icon: {
      type: String,
      default: ''
    }
  },
  components : {
    GOHeader
  }
}
</script>
