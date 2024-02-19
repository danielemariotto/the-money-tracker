<script setup lang="ts">
import { ref } from 'vue'
import insertTransaction from '@/components/insertTransaction.vue'
const earning_list  = ref([{digits: 200, category: 'ecommerce'}, {digits: 300, category: 'investment'}])
const expenses_list  = ref([{digits: 33, category: 'shopping'}, {digits: 45, category: 'shopping'}])
const enterOperation = () => {
    console.log('add entry')
}
</script>
<template>
    <div>
        <v-container>
            Daily
            <v-row>
              <v-col>
              EARNING
                    <div v-for="row, i in earning_list" :key="i">
                        {{row.digits}} - {{row.category}}
                    </div>
              </v-col>
              <v-col
              >EXPENSES
                    <div v-for="row, i in expenses_list" :key="i">
                        {{row.digits}} - {{row.category}}
                    </div>
              </v-col>
        </v-row>
        <v-btn @click="enterOperation">add entry</v-btn>
          </v-container>
        <insertTransaction></insertTransaction>
    </div>
</template>
<style>
    
</style>