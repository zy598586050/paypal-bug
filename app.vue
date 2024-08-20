<template>
  <div id="paypal"></div>
</template>

<script setup lang="ts">
import { loadScript } from '@paypal/paypal-js'

loadScript({
  clientId: 'xxxxx'
}).then((result: any) => {
  result?.Buttons()?.render('#paypal')
})
</script>