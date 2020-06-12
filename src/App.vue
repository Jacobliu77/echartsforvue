<template>
  <div id="app">
    <dv-full-screen-container>
      <dv-border-box-11 title="大屏数据动态展示" style=" overflow: hidden; ">
        <div id="top">
          <div class="left"><dv-border-box-8  style="padding:3px" >
            <dv-active-ring-chart :config="config1" style="width:98%;height:280px" />
            </dv-border-box-8></div>
          <div class="middle">
              <!-- <dv-border-box-6 style="padding:10px"> -->
                  <dv-flyline-chart-enhanced :config="config2" style="width:100%;height:280px;" />
              <!-- </dv-border-box-6> -->
          </div>
          <div class="right">
              <dv-border-box-8 :reverse="true" style="padding:3px">
                  <dv-scroll-board :config="config3" style="width:100%;height:280px" />
              </dv-border-box-8>
          </div>
        </div>
        <div id="bottom">
          <div class="left">
            <dv-border-box-1>
               <dv-charts :option="optionb"  style="width:100%;height:280px" />
            </dv-border-box-1>
          </div>
          <div class="middle">
            <dv-border-box-9>
              <dv-charts :option="optiona"  style="width:100%;height:280px" />
            </dv-border-box-9>
          </div>
          <div class="right">
            <dv-border-box-1>
              <dv-charts :option="optionc"  style="width:100%;height:280px" />
            </dv-border-box-1>
          </div>
        </div>
        <dv-loading>Loading...</dv-loading>
      </dv-border-box-11> 
    </dv-full-screen-container>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return{
      config1:{
        radius: '40%',
        activeRadius: '45%',
        data: [
          {
            name: '周口',
            value: 55
          },
          {
            name: '南阳',
            value: 120
          },
          {
            name: '西峡',
            value: 78
          },
          {
            name: '驻马店',
            value: 66
          },
          {
            name: '新乡',
            value: 80
          }
        ],
        digitalFlopStyle: {
          fontSize: 20
        },
        showOriginValue: true
      },
      config2:{
                points: [
            {
              name: '郑州',
              coordinate: [0.48, 0.35],
              icon: {
                src: require('./assets/mapCenterPoint.png'),
                width: 30,
                height: 30
              },
              text: {
                color: '#fb7293'
              }
            },
            {
              name: '新乡',
              coordinate: [0.52, 0.23]
            },
            {
              name: '焦作',
              coordinate: [0.43, 0.29]
            },
            {
              name: '开封',
              coordinate: [0.59, 0.35]
            },
            {
              name: '许昌',
              coordinate: [0.53, 0.47]
            },
            {
              name: '平顶山',
              coordinate: [0.45, 0.54]
            },
            {
              name: '洛阳',
              coordinate: [0.36, 0.38]
            },
            {
              name: '周口',
              coordinate: [0.62, 0.55]
            },
            {
              name: '漯河',
              coordinate: [0.56, 0.56]
            },
            {
              name: '南阳',
              coordinate: [0.37, 0.66]
            },
            {
              name: '信阳',
              coordinate: [0.55, 0.81]
            },
            {
              name: '驻马店',
              coordinate: [0.55, 0.67]
            },
            {
              name: '济源',
              coordinate: [0.37, 0.29]
            },
            {
              name: '三门峡',
              coordinate: [0.20, 0.36]
            },
            {
              name: '商丘',
              coordinate: [0.76, 0.41]
            },
            {
              name: '鹤壁',
              coordinate: [0.59, 0.18]
            },
            {
              name: '濮阳',
              coordinate: [0.68, 0.17]
            },
            {
              name: '安阳',
              coordinate: [0.59, 0.10]
            }
          ],
          lines: [
            {
              source: '新乡',
              target: '郑州'
            },
            {
              source: '焦作',
              target: '郑州'
            },
            {
              source: '开封',
              target: '郑州'
            },
            {
              source: '许昌',
              target: '郑州'
            },
            {
              source: '平顶山',
              target: '郑州'
            },
            {
              source: '洛阳',
              target: '郑州'
            },
            {
              source: '周口',
              target: '郑州'
            },
            {
              source: '漯河',
              target: '郑州'
            },
            {
              source: '南阳',
              target: '郑州'
            },
            {
              source: '信阳',
              target: '郑州'
            },
            {
              source: '驻马店',
              target: '郑州'
            },
            {
              source: '济源',
              target: '郑州'
            },
            {
              source: '三门峡',
              target: '郑州'
            },
            {
              source: '商丘',
              target: '郑州'
            },
            {
              source: '鹤壁',
              target: '郑州'
            },
            {
              source: '濮阳',
              target: '郑州'
            },
            {
              source: '安阳',
              target: '郑州'
            }
          ],
          icon: {
            show: true,
            src: require('./assets/mapPoint.png')
          },
          text: {
            show: true,
          },
          bgImgSrc: require( './assets/map.jpg')
      },
      config3:{
        header: ['列1', '列2', '列3'],
        data: [
          ['行1列1', '行1列2', '行1列3'],
          ['行2列1', '行2列2', '行2列3'],
          ['行3列1', '行3列2', '行3列3'],
          ['行4列1', '行4列2', '行4列3'],
          ['行5列1', '行5列2', '行5列3'],
          ['行6列1', '行6列2', '行6列3'],
          ['行7列1', '行7列2', '行7列3'],
          ['行8列1', '行8列2', '行8列3'],
          ['行9列1', '行9列2', '行9列3'],
          ['行10列1', '行10列2', '行10列3']
        ]
      },
      optiona:{
          series: [
            {
              type: 'gauge',
              startAngle: -Math.PI / 2,
              endAngle: Math.PI * 1.5,
              arcLineWidth: 10,
              data: [
                { name: 'A', value: 25, gradient: ['#03c2fd', '#1ed3e5', '#2fded6'] },
                { name: 'B', value: 45, gradient: ['#03c2fd', '#1ed3e5', '#2fded6'], radius: '53%' },
                { name: 'C', value: 65, gradient: ['#03c2fd', '#1ed3e5', '#2fded6'], radius: '46%' },
                { name: 'D', value: 35, gradient: ['#03c2fd', '#1ed3e5', '#2fded6'], radius: '39%' },
                { name: 'E', value: 25, gradient: ['#03c2fd', '#1ed3e5', '#2fded6'], radius: '32%' }
              ],
              axisLabel: {
                show: false
              },
              axisTick: {
                show: false
              },
              pointer: {
                show: false
              },
              dataItemStyle: {
                lineCap: 'round'
              },
              backgroundArc: {
                show: false
              },
              details: {
                show: true,
                formatter: '{name}占比{value}%',
                position: 'start',
                offset: [-10, 0],
                style: {
                    fill: '#1ed3e5',
                    fontSize: 10,
                    textAlign: 'right',
                }
              }
            }
          ]
      },
      optionb:{
        title: {
          text: '气温与降雨量走势图'
        },
        legend: {
          data: ['降雨量', '气温'],
          bottom: 10
        },
        xAxis: {
          data: [
          '一月份', '二月份', '三月份', '四月份', '五月份', '六月份',
          '七月份', '八月份', '九月份', '十月份', '十一月份', '十二月份'
          ],
          axisLabel: {
            style: {
              rotate: 20,
              textAlign: 'left',
              textBaseline: 'top'
            }
          },
          axisTick: {
            show: false
          }
        },
        yAxis: [
          {
            name: '降雨量',
            data: 'value',
            min: 0,
            max: 300,
            interval: 50,
            splitLine: {
              style: {
                lineDash: [3,3]
              }
            },
            axisLabel: {
              formatter: '{value} ml'
            },
            axisTick: {
              show: false
            }
          },
          {
            name: '气温',
            data: 'value',
            position: 'right',
            min: 0,
            max: 30,
            interval: 5,
            splitLine: {
              show: false
            },
            axisLabel: {
              formatter: '{value} °C',
            },
            axisTick: {
              show: false
            }
          }
        ],
        series: [
          {
            name: '降雨量',
            data: [
              175, 125, 90, 130, 45, 65,
              65, 47, 50, 52, 45, 37
            ],
            type: 'bar',
            gradient: {
              color: ['#37a2da', '#67e0e3']
            },
            animationCurve: 'easeOutBounce'
          },
          {
            name: '气温',
            data: [
            23, 18, 16, 14, 10, 8,
            6, 6, 6, 6, 6, 5
            ],
            type: 'line',
            yAxisIndex: 1,
            animationCurve: 'easeOutBounce'
          }
        ]
      },
      optionc:{
        title: {
          text: '周销售额趋势'
        },
        legend: {
          data: ['系列A', '系列B', '系列C']
        },
        xAxis: {
          name: '第一周',
          data: ['周一', '周二', '周三', '周四', '周五', '周六', '周日']
        },
        yAxis: {
          name: '销售额',
          data: 'value'
        },
        series: [
          {
            name: '系列A',
            data: [1200, 2230, 1900, 2100, 3500, 4200, 3985],
            type: 'line',
            stack: 'a',
            fill: {
              show: true
            },
            lineArea: {
              show: true,
              gradient: ['rgba(251, 114, 147, 0.6)', 'rgba(251, 114, 147, 0)']
            },
             lineStyle: {
                stroke: 'rgba(251, 114, 147, 1)',
                lineDash: [3, 3]
              },
              linePoint: {
                style: {
                  stroke: 'rgba(251, 114, 147, 1)'
                }
              }
          },
          {
            name: '系列B',
            data: [1200, 2230, 1900, 2100, 3500, 4200, 3985],
            type: 'line',
            stack: 'a',
            smooth: true,
            lineArea: {
              show: true,
              gradient: ['rgba(55, 162, 218, 0.6)', 'rgba(55, 162, 218, 0)']
            }
          },
          {
            name: '系列C',
            data: [1200, 2230, 1900, 2100, 3500, 4200, 3985],
            type: 'line',
            stack: 'a',
            lineStyle: {
              stroke: 'rgba(100, 255, 0, 1)',
              lineDash: [5, 5]
            },
            lineArea: {
              show: true,
              gradient: ['rgba(100, 255, 0, 0.6)', 'rgba(100, 255, 0, 0)']
            },
            linePoint: {
                style: {
                  stroke: 'rgba(100, 255, 0, 1)'
                }
            }
          }
        ]
      }
    }  
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
  width:100%;
  height:100vh;
  margin: 0 ;
  padding: 0 ;
  background-color:#000;

}
#top {
  height:50%;
  margin:0;
  padding:0;
  width:97%;
  margin-top:4.8%
}
#bottom {
  height:50%;
  margin:0;
  padding:0;
  width:97%;
}
.left {
  margin:0;
  padding:0;
  width:30%;
  margin-right:1.5%;
  float:left;
  margin-left:3%;
}
.middle {
  margin:0;
  padding:0;
  width:34%;
  margin-right:1.5%;
  float:left;
}
.right {
  margin:0;
  padding:0;
  width:30%;
  float:left;
}
</style>
