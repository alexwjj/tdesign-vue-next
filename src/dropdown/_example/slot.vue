<template>
  <t-space>
    <t-dropdown :min-column-width="88" trigger="click" @click="handleClick">
      <t-button variant="text">下拉菜单</t-button>
      <template #dropdown>
        <t-dropdown-menu>
          <t-dropdown-item :value="1">操作一</t-dropdown-item>
          <t-dropdown-item :value="2">操作二</t-dropdown-item>
        </t-dropdown-menu>
      </template>
    </t-dropdown>
  </t-space>
</template>
<script setup>
const handleClick = (data, { e }) => {
  console.log(data);
  e.preventDefault();
};
</script>
