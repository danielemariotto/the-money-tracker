<template>
  <div>
    Import:<input type="number">
    <v-btn @click="showTransactionDetail">add</v-btn>
    <transactionDetail v-if="transactionDetailFlag"></transactionDetail>
  </div>
</template>

<script setup>
import {ref} from 'vue'
import transactionDetail from '@/components/transactionDetail.vue'
const transactionDetailFlag = ref(false)
const showTransactionDetail = () => {
    transactionDetailFlag.value = !transactionDetailFlag.value
}
</script>

<style>

</style>