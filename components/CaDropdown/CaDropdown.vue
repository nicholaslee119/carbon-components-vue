<template>
  <ul data-dropdown data-value class="bx--dropdown" tabindex="0">
    <li class="bx--dropdown-text">{{defaultText}}</li>
    <svg class="bx--dropdown__arrow" width="10" height="5" viewBox="0 0 10 5" fill-rule="evenodd">
      <path d="M10 0L5 5 0 0z"></path>
    </svg>
    <li>
      <ul class="bx--dropdown-list">
        <slot></slot>
      </ul>
    </li>
  </ul>
</template>

<script>
import { Dropdown } from 'carbon-components';

export default {
  name: 'ca-dropdown',
  props: {
    value: null,
    defaultText: {
      type: String,
      default: 'Dropdown label',
    },
  },
  data() {
    return {
      dropdown: null,
    };
  },
  mounted() {
    this.dropdown = Dropdown.create(this.$el);
  },
};
</script>

<style></style>
