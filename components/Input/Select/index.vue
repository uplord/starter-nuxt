<template>
  <div class="field">
    <label v-if="label" :for="inputId">{{ label }}</label>
    <div class="input-wrap select-wrap">
      <select
        :id="inputId"
        class="input"
        :value="value"
        :disabled="disabled"
        v-bind="{
          ...$attrs,
          onChange: ($event) => { $emit('update:value', $event.target.value) }
        }"
      >
        <option
          v-for="option in options"
          :value="option"
          :key="option"
          :selected="option === modelValue"
        >{{ option }}</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    label: String,
    value: [String, Number],
    disabled: Boolean,
    options: Array
  },
  computed: {
    inputId() {
      return `${this.label.replace(/\s+/g, '-').toLowerCase()}-select`;
    }
  }
}
</script>

<style lang="less">
  @import '../style';
  @import 'style';
</style>
