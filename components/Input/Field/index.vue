<template>
  <div class="field">
    <label v-if="label" :for="inputId">{{ label }}</label>
    <div class="input-wrap">
      <input
        v-bind="$attrs"
        :id="inputId"
        class="input"
        :placeholder="placeholder"
        :max="max"
        :value="value"
        :disabled="disabled"
        @input="$emit('update:value', $event.target.value)"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    label: String,
    placeholder: String,
    max: String,
    value: [String, Number],
    disabled: Boolean,
  },
  computed: {
    inputId() {
      return `${this.label.replace(/\s+/g, '-').toLowerCase()}-input`;
    }
  }
}
</script>

<style lang="less" scoped>
  @import '../style';
  @import 'style';
</style>