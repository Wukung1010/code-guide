<script lang="ts" setup></script>

<template>
  <button :class="$style.button">
    <slot></slot>
  </button>
</template>

<style module>
.button {
  padding: 10px 20px;
  font-size: 16px;
  color: var(--myapp-font-color);
  background-color: #006eda;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>
