<template>
  <div class="flares-input">
    <input
      class="flares-input__inner"
      :class="{ 'is-disabled': disabled }"
      :type="type"
      :placeholder="placeholder"
      :name="name"
      :disabled="disabled"
      :value="value"
      @input="handleInput"
    />
  </div>
</template>

<script lang="ts">
export default {
  name: 'Input',
  props: {
    placeholder: {
      type: String,
      default: ''
    },
    type: {
      type: String,
      default: 'text'
    },
    name: {
      type: String,
      default: ''
    },
    disabled: {
      type: Boolean,
      default: false
    },
    value: {
      type: String,
      default: ''
    }
  },
  setup(props, context) {
    const handleInput = e => {
      context.emit('update:value', e.target.value)
    }
    return { handleInput }
  }
}
</script>

<style lang="scss" scoped>
.flares-input {
  position: relative;
  font-size: 14px;
  display: inline-block;

  .flares-input__inner {
    display: inline-block;
    background-color: #fff;
    border-radius: 4px;
    border: 1px solid #dcdfe6;
    box-sizing: border-box;
    color: #606266;
    font-size: inherit;
    height: 40px;
    line-height: 40px;
    outline: none;
    padding: 0 15px;
    transition: border-color 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
    width: 100%;

    &:focus {
      outline: none;
      border-color: #fc6e51;
    }

    &.is-disabled {
      background-color: #f5f7fa;
      border-color: #e4e7ed;
      color: #c0c4cc;
      cursor: not-allowed;
    }
  }
}
</style>
