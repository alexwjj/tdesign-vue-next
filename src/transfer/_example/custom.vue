<template>
  <div>
    <t-transfer :data="list">
      <template #title="props">
        <div>{{ props.type === 'target' ? '目标' : '来源' }}</div>
      </template>
      <template #operation="props">
        {{ props.direction === 'left' ? '移除' : '加入' }}
      </template>
      <template #footer="props">
        <div style="padding: 10px; border-top: 1px solid #e7e7e7">
          <span v-if="props.type === 'source'">选中并加入</span>
          <span v-else>选中并移除</span>
        </div>
      </template>
    </t-transfer>
  </div>
</template>
<script setup>
const list = [];
for (let i = 0; i < 20; i++) {
  list.push({
    value: i.toString(),
    label: `内容${i + 1}`,
  });
}
</script>
