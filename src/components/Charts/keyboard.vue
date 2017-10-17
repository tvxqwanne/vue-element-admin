<template>
  <div :class="className" :id="id" :style="{height:height,width:width}"></div>
</template>

<script>
import echarts from 'echarts'

export default {
  props: {
    className: {
      type: String,
      default: 'chart'
    },
    id: {
      type: String,
      default: 'chart'
    },
    width: {
      type: String,
      default: '200px'
    },
    height: {
      type: String,
      default: '200px'
    }
  },
  data() {
    return {
      chart: null
    }
  },
  mounted() {
    this.initChart()
  },
  beforeDestroy() {
    if (!this.chart) {
      return
    }
    this.chart.dispose()
    this.chart = null
  },
  methods: {
    initChart() {
      this.chart = echarts.init(document.getElementById(this.id))

      const xAxisData = []
      const yAxisData = [0.00, 0.01, 0.00, 0.00, 0.05, 0.44, 1.45, 1.53, 1.69, 1.50, 1.62, 1.45, 2.05, 1.85, 1.39, 1.42, 1.17, 0.60, 0.56, 0.54, 0.56, 0.57, 0.02]
      for (let i = 0; i < 24; i++) {
        xAxisData.push(i + ':00')
      // data.push(Math.round(Math.random() * 2 + 3))
      }
      // for (let i = 0; i < 24; i++) {
      //   data[i] = [xAxisData[i], yAxisData[i] + '立方米', yAxisData[i]]
      // }
      // const data = [
      //   [0 + ':00', 0.00 + '立方米'],
      //   [1 + ':00', 0.01 + '立方米'],
      //   [2 + ':00', 0.00 + '立方米'],
      //   [3 + ':00', 0.00 + '立方米'],
      //   [4 + ':00', 0.05 + '立方米'],
      //   [5 + ':00', 0.44 + '立方米'],
      //   [6 + ':00', 1.45 + '立方米']
      // ]

      this.chart.setOption(
        {
          backgroundColor: '#08263a',
          tooltip: {
            trigger: 'axis',
            formatter: '时　间: {b0} <br /> {a0}: {c0} 立方米'
            // axisPointer: {
            //   axis: 'x',
            //   label: {
            //     show: true,
            //     name: 'shis'
            //     // percision: 2,
            //     // formatter: '{value} 立方米'
            //   }
            // }
          },
          xAxis: {
            show: true,
            data: xAxisData,
            name: '时间'
          },
          visualMap: {
            show: true,
            min: 0,
            max: 50,
            dimension: 0,
            inRange: {
              color: ['#4a657a', '#308e92', '#b1cfa5', '#f5d69f', '#f5898b', '#ef5055']
            }
          },
          yAxis: {
            axisLine: {
              show: true
            },
            axisLabel: {
              textStyle: {
                color: '#4a657a'
              }
            },
            splitLine: {
              show: true,
              lineStyle: {
                color: '#08263f'
              }
            },
            axisTick: {},
            name: '小时用水量/立方米'
          },
          series: [{
            type: 'bar',
            data: yAxisData,
            name: '用水量',
            itemStyle: {
              normal: {
                barBorderRadius: 5,
                shadowBlur: 10,
                shadowColor: '#111'
              }
            },
            animationEasing: 'elasticOut',
            animationEasingUpdate: 'elasticOut',
            animationDelay(idx) {
              return idx * 20
            },
            animationDelayUpdate(idx) {
              return idx * 20
            }
          }]
        })
    }
  }
}
</script>
