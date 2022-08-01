<template src='./ValidationRules.html'></template>
<script>
export default {
  name: 'ValidationRules',
  props: {
    isValid: {
      type: Boolean,
      default: null
    },
    message: {
      type: String,
      default: null
    }
  },
  computed: {
    rulesIcon() {
      if (this.isValid) return 'valid'
      if (this.isValid === false) return 'invalid'
      return ''
    }
  }
}
</script>
<style scoped lang='scss' src='./ValidationRules.scss'></style>
