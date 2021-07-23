<template>
  <d2-container type='full'>
    <el-row :gutter='24'>
      <el-col :span='6'>
        <el-card shadow='never' class='d2-card d2-mb'>
          <div class='group'>
            <countup :endVal='64' title='Tx Count'/>
          </div>
        </el-card>
      </el-col>
      <el-col :span='6'>
        <el-card shadow='never' class='d2-card d2-mb'>
          <div class='group'>
            <countup :endVal='263' title='Node Count'/>
          </div>
        </el-card>
      </el-col>
      <el-col :span='6'>
        <el-card shadow='never' class='d2-card d2-mb'>
          <div class='group'>
            <countup :endVal='200' title='Block height'/>
          </div>
        </el-card>
      </el-col>
      <el-col :span='6'>
        <el-card shadow='never' class='d2-card d2-mb'>
          <div class='group'>
            <countup :endVal='890' title='Tx Count'/>
          </div>
        </el-card>
      </el-col>
    </el-row>

    <el-row :gutter='24'>
      <el-col :span='12'>
        <el-card shadow='never' class='d2-card d2-mb'>
          <div class='group'>
            <ve-line :data="chartData" :title='title'/>
          </div>
        </el-card>
      </el-col>
      <el-col :span='12'>
        <el-card shadow='never' class='d2-card d2-mb'>
          <div class='group'>
            <ve-line :data="chartData"/>
            <p class='table-title'>表格 - 2 </p>
          </div>
        </el-card>
      </el-col>
    </el-row>

  </d2-container>
</template>

<script type='text/babel'>
import countup from '@/components/count-up'
import 'echarts/lib/component/title'

export default {
  name: 'page2',
  components: {
    countup
  },
  data () {
    return {
      chartData: {
        columns: ['日期', '访问用户', '下单用户', '下单率'],
        rows: [
          { 日期: '1/1', 访问用户: 1393, 下单用户: 1093, 下单率: 0.32 },
          { 日期: '1/2', 访问用户: 3531, 下单用户: 3230, 下单率: 0.26 },
          { 日期: '1/3', 访问用户: 2923, 下单用户: 2623, 下单率: 0.76 },
          { 日期: '1/4', 访问用户: 1723, 下单用户: 1423, 下单率: 0.49 },
          { 日期: '1/5', 访问用户: 3792, 下单用户: 3492, 下单率: 0.323 },
          { 日期: '1/6', 访问用户: 4593, 下单用户: 4293, 下单率: 0.78 }
        ]
      },
      title: {
        text: 'a         test title for charts.',
        textAlign: 'auto',
        left: 'center',
        bottom: '0%',
        textStyle: {
          color: 'black'
        }
      }
    }
  }
}
</script>

<style scoped>
.table-title {
  text-align: center;
}
</style>
