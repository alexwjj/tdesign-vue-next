<template>
  <div class="tdesign-demo-block-column" style="width: 100%">
    <div class="t-tdesign-demo__tag-input">
      <label>禁用状态：</label>
      <t-tag-input :value="tags1" disabled />
    </div>

    <div class="t-tdesign-demo__tag-input">
      <label>只读状态：</label>
      <t-tag-input :value="tags2" tips="这是普通文本提示" readonly />
    </div>

    <div class="t-tdesign-demo__tag-input">
      <label>成功状态：</label>
      <t-tag-input v-model="tags3" status="success" tips="校验通过文本提示" clearable />
    </div>

    <div class="t-tdesign-demo__tag-input">
      <label>告警状态：</label>
      <t-tag-input v-model="tags4" status="warning" tips="校验不通过文本提示" clearable />
    </div>

    <div class="t-tdesign-demo__tag-input">
      <label>错误状态：</label>
      <t-tag-input v-model="tags5" status="error" tips="校验存在严重问题文本提示" clearable />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const tags1 = ref(['Vue', 'React', 'Miniprogram']);
const tags2 = ref(['Vue', 'React', 'Miniprogram']);
const tags3 = ref(['Vue', 'React', 'Miniprogram']);
const tags4 = ref(['Vue', 'React', 'Miniprogram']);
const tags5 = ref(['Vue', 'React', 'Miniprogram']);
</script>

<style lang="less">
.t-tdesign-demo__tag-input {
  display: flex;
  align-items: baseline;
  > label {
    width: 100px;
  }
}
</style>
