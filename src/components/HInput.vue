<!--
 * @Author: Bamboo
 * @AuthorEmail: bamboo8493@126.com
 * @AuthorDescription:
 * @Modifier:
 * @ModifierEmail:
 * @ModifierDescription:
 * @Date: 2020-05-01 22:45:32
 * @LastEditTime: 2020-05-01 22:47:51
-->
<template>
  <div class="h-input">
    <input :type="type" :value="value" v-bind="$attrs" @input="onInput($event)">
  </div>
</template>

<script>
  export default {
    name: 'h-input',
    data() {
      return {}
    },
    props: {
      type: {
        type: String,
        default: 'text'
      },
      value: {
        type: String,
        default: ''
      },
    },
    methods: {
      onInput(e) {
        this.$emit('input', e.target.value)
      }
    }
  }
</script>

<style lang="sass" scoped></style>