<template>
  <v-container>
    <v-row align="center" justify="space-between">
      <v-col cols="auto" md="auto">
        <h1 class="text-h4">
          {{ $t('envelope') + ': ' + $t('overflow-envelope') }}
        </h1>
      </v-col>
    </v-row>
    <v-row justify="space-between">
      <v-col cols="auto">
        <v-table>
          <tbody>
            <tr>
              <td>{{ $t('balance') }}</td>
              <td>{{ balance }}</td>
            </tr>
          </tbody>
        </v-table>
      </v-col>
      <v-col cols="auto" class="d-flex flex-column">
        <v-btn class="mb-2">{{ $t('deposit') }}</v-btn>
        <v-btn class="mb-2">{{ $t('withdraw') }}</v-btn>
        <v-btn>{{ $t('transfer') }}</v-btn>
      </v-col>
      <v-col cols="auto" class="d-flex flex-column">
        <v-btn @click="changeSettingsClicked" class="mb-2">{{
          $t('change-settings')
        }}</v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="8">
        <LastTransactions />
      </v-col>
      <v-col cols="12" md="4">
        <BarChart />
      </v-col>
    </v-row>
  </v-container>
</template>
<script setup>
import router from '@/router'
import { formatCurrency } from '@/utils.js'

const balance = formatCurrency(125.0)

const changeSettingsClicked = () => {
  router.push({
    path: '/editoverflow'
  })
}
</script>
