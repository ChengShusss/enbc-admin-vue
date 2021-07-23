<template>
  <d2-container type="full">
    <countup/>
  </d2-container>
</template>

<script>
import countup from '@/components/count-up'
export default {
  name: 'dashboard',
  data: function () {
    return {
      blockchain: 20
    }
  },
  components: {
    countup
  }
}
</script>
