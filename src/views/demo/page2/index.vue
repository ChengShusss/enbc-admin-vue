<template>
  <d2-container type="full">
    <el-row :gutter="20">
      <el-col :span="6">
        <el-card shadow="never" class="d2-card d2-mb">
          <div class="group">
            <countup/>
          </div>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card shadow="never" class="d2-card d2-mb">
          <div class="group">
            <countup/>
          </div>
        </el-card>
      </el-col>
    </el-row>

  </d2-container>
</template>

<script type='text/babel'>
import countup from '@/components/count-up'

export default {
  name: 'page2',
  components: {
    countup
  }
}
</script>
