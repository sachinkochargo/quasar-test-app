<template>
    <!-- <GOHeader  > -->
      <MyButton msg="test" />
    <!-- </GOHeader> -->
</template>

<script>
import { MyButton } from 'go-component-library';

export default {
  name: 'Demo',
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
    MyButton,
    // GOHeader
  }
}
</script>
