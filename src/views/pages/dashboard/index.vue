<template>
  <d2-container type="full">
    <el-row :gutter='24'>
      <el-col :span='3'>
        <countup />
      </el-col>
      <el-col :span='4'>
        <el-card shadow='never'
                 class='d2-card d2-mb'>
          <div class='group'>
            <countup :endVal='64'
                     title='Tx Count' />
          </div>
        </el-card>
      </el-col>
    </el-row>
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
