<template>
  <v-card
    @click="CreateNewEnvelopenvelopeClicked"
    variant="tonal"
    min-height="180"
    class="d-flex flex-column align-center justify-center"
  >
    <v-card-item class="text-center">
      <v-card-title>{{ $t('new-envelope') }}</v-card-title>
    </v-card-item>
    <v-card-actions>
      <v-btn icon="mdi-plus" variant="tonal"></v-btn>
    </v-card-actions>
  </v-card>
</template>
<script setup>
import router from '@/router/index.js'

function CreateNewEnvelopenvelopeClicked() {
  router.push({
    path: '/createenvelope'
  })
}
</script>
