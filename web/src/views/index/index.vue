<template>
  <el-card>
  <generate-form ref="generateFormRef" :data="widgetForm">
  </generate-form>
  <el-button type="primary" @click="handleSubmit">提交</el-button></el-card>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const generateFormRef = ref()
const widgetForm = {"list":[{"type":"number","label":"计数器","options":{"defaultValue":0,"width":"","min":0,"max":100,"step":1,"precision":0,"controlsPosition":"","labelHide":false,"disabled":false,"readonly":false,"rules":[]},"key":"xr3dmyfp","name":"number_tclwb2"},{"type":"select","label":"下拉选择框","options":{"defaultValue":"","width":"","multiple":false,"placeholder":null,"labelHide":false,"filterable":false,"clearable":false,"disabled":false,"options":[{"label":"标签1","value":"value1"},{"label":"标签2","value":"value2"},{"label":"标签3","value":"value3"}],"optionsType":"option","requestUrl":"","dictName":"","props":{"value":"value","label":"label"},"rules":[]},"key":"x1hv1j81","name":"select_dxdeo5"},{"type":"date","label":"日期选择器","options":{"defaultValue":"","width":"","type":"date","format":"YYYY-MM-DD","placeholder":null,"startPlaceholder":null,"endPlaceholder":null,"labelHide":false,"clearable":true,"disabled":false,"rules":[]},"key":"skl2r5xw","name":"date_pd63w9"},{"type":"text","label":"文字","options":{"defaultValue":"This is a text"},"key":"yfh0e5db","name":"text_yo3xu2"}],"config":{"size":"default","labelWidth":100,"labelPosition":"right","style":""}}

const handleSubmit = () => {
  generateFormRef.value.getData().then((data: any) => {
    console.log(data)
    // data 表单数据
  }).catch((error: any) => {
    // data failed
  })
}
</script>
    