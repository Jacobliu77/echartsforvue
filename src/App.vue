<template>
  <div id="app">
    <dv-full-screen-container>
      <dv-border-box-11 title="大屏数据动态展示" style=" overflow: hidden; ">
        <div id="top">
          <div class="left"><dv-border-box-8 >
            <dv-active-ring-chart :config="config1" style="width:100%;height:300px" />
            </dv-border-box-8></div>
          <div class="middle">
              <dv-border-box-6>
                  <dv-flyline-chart-enhanced :config="config2" style="width:100%;height:300px;" />
              </dv-border-box-6>
          </div>
          <div class="right"><dv-border-box-8 :reverse="true">dv-border-box-8</dv-border-box-8></div>
        </div>
        <div id="bottom">
          <div class="left"><dv-border-box-1>dv-border-box-1</dv-border-box-1></div>
          <div class="middle"><dv-border-box-9>dv-border-box-9</dv-border-box-9></div>
          <div class="right"><dv-border-box-1>dv-border-box-1</dv-border-box-1></div>
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
                src: './assets/mapCenterPoint.png',
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
            src: './assets/mapPoint.png'
          },
          text: {
            show: true,
          },
          bgImgSrc: './assets/map.jpg'
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
