<!-- html结构，css自己扒就行了 -->
<template>
  <div class="aside aside-count">
    <h3>
      <svg class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg">
        <path d="M864.801 895.471h-33.56v-96.859c0-126.081-73.017-235.093-179.062-287.102 106.046-52.01 179.062-161.022 179.062-287.102v-96.859h33.56c17.301 0 31.325-14.327 31.325-32 0-17.673-14.024-32-31.325-32H159.018c-17.3 0-31.325 14.327-31.325 32 0 17.673 14.025 32 31.325 32h33.02v96.859c0 126.08 73.016 235.092 179.061 287.102-106.046 52.009-179.062 161.02-179.062 287.101v96.859h-33.02c-17.3 0-31.325 14.326-31.325 32s14.025 32 31.325 32H864.8c17.301 0 31.325-14.326 31.325-32s-14.023-31.999-31.324-31.999zM256.05 222.427v-94.878h513.046v94.878c0 141.674-114.85 256.522-256.523 256.522-141.674 0-256.523-114.848-256.523-256.522z m513.046 673.044H256.05v-94.879c0-141.674 114.849-256.521 256.523-256.521 141.673 0 256.523 114.848 256.523 256.521v94.879z" p-id="29837"></path>
        <path d="M544.141 384c0-17.69-14.341-32.031-32.031-32.031-71.694 0-127.854-56.161-127.854-127.855 0-17.69-14.341-32.032-32.031-32.032s-32.032 14.341-32.032 32.032c0 107.617 84.3 191.918 191.917 191.918 17.69 0 32.031-14.342 32.031-32.032z" p-id="29838"></path>
      </svg>
      <span>人生倒计时</span>
      <span class="line"></span>
    </h3>
    <div class="item" v-for="(item, index) in timelife" :key="index">
      <div class="title">
        {{ item.title }}
        <span class="text">{{ item.num }}</span>
        {{ item.endTitle }}
      </div>
      <div class="progress">
        <div class="progress-bar">
          <div class="progress-bar-inner" :class="'progress-bar-inner-' + index" :style="{ width: item.percent }"></div>
        </div>
        <div class="progress-percentage">{{ item.percent }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timelife: [
        { title: '今日已经过去', endTitle: '小时', num: 0, percent: '0%' },
        { title: '这周已经过去', endTitle: '天', num: 0, percent: '0%' },
        { title: '本月已经过去', endTitle: '天', num: 0, percent: '0%' },
        { title: '今年已经过去', endTitle: '个月', num: 0, percent: '0%' }
      ]
    }
  },
  mounted() {
    this.calculateTime();
    setInterval(this.calculateTime, 1000);
  },
  methods: {
    /* 计算时间 */
    calculateTime() {
      {
        let nowDate = +new Date();
        let todayStartDate = new Date(new Date().toLocaleDateString()).getTime();
        let todayPassHours = (nowDate - todayStartDate) / 1000 / 60 / 60;
        let todayPassHoursPercent = (todayPassHours / 24) * 100;
        this.timelife[0].num = parseInt(todayPassHours);
        this.timelife[0].percent = parseInt(todayPassHoursPercent) + '%';
      }
      {
        let weeks = { 0: 7, 1: 1, 2: 2, 3: 3, 4: 4, 5: 5, 6: 6 };
        let weekDay = weeks[new Date().getDay()];
        let weekDayPassPercent = (weekDay / 7) * 100;
        this.timelife[1].num = parseInt(weekDay);
        this.timelife[1].percent = parseInt(weekDayPassPercent) + '%';
      }
      {
        let year = new Date().getFullYear();
        let date = new Date().getDate();
        let month = new Date().getMonth() + 1;
        let monthAll = new Date(year, month, 0).getDate();
        let monthPassPercent = (date / monthAll) * 100;
        this.timelife[2].num = date;
        this.timelife[2].percent = parseInt(monthPassPercent) + '%';
      }
      {
        let month = new Date().getMonth() + 1;
        let yearPass = (month / 12) * 100;
        this.timelife[3].num = month;
        this.timelife[3].percent = parseInt(yearPass) + '%';
      }
    }
  }
}
</script>
<style scoped="scoped">
.item .title {
  font-size: 12px;
  color: #909399;
  margin-bottom: 5px;
  display: flex;
  align-items: center;
}
.item .progress {
  display: flex;
  align-items: center;
}
.item .title span {
  color: red;
  font-weight: 500;
  font-size: 14px;
  margin: 0 5px;
}
.item .progress .progress-bar {
  height: 10px;
  border-radius: 5px;
  overflow: hidden;
  background: #EBEEF5;
  width: 0;
  min-width: 0;
  flex: 1;
  margin-right: 5px;
}
 .item .progress .progress-bar .progress-bar-inner {
  width: 0;
  height: 100%;
  border-radius: 5px;
  transition: width 0.35s;
  -webkit-animation: progress 750ms linear infinite;
  animation: progress 750ms linear infinite;
}
 .item .progress .progress-bar .progress-bar-inner-0 {
  /*background: #ffd980;*/
  background-image: linear-gradient(135deg, #f7ba2a 25%, transparent 25%, transparent 50%, #f7ba2a 50%, #f7ba2a 75%, transparent 75%, transparent 100%);
  background-size: 30px 30px;
}
.item .progress .progress-bar .progress-bar-inner-1 {
  /*background: #ffd980;*/
  background-image: linear-gradient(
    135deg
    , #f7ba2a 25%, transparent 25%, transparent 50%, #f7ba2a 50%, #f7ba2a 75%, transparent 75%, transparent 100%);
  background-size: 30px 30px;
}
.item .progress .progress-bar .progress-bar-inner-2 {
  /*background: #ffa9a9;*/
  background-image: linear-gradient(
    135deg
    , #ff4949 25%, transparent 25%, transparent 50%, #ff4949 50%, #ff4949 75%, transparent 75%, transparent 100%);
  background-size: 30px 30px;
}
.item .progress .progress-bar .progress-bar-inner-3 {
  /*background: #67c23a;*/
  background-image: linear-gradient(
    135deg
    , #4f9e28 25%, transparent 25%, transparent 50%, #4f9e28 50%, #4f9e28 75%, transparent 75%, transparent 100%);
  background-size: 30px 30px;
}
 @keyframes progress {
   0% {
     background-position: 0 0;
   }
   100% {
     background-position: 30px 0;
   }
 }
.aside h3 .line {
  width: 10px;
  height: 1px;
  background: #54b5db;
  margin-left: 12px;
}
 .aside h3 .icon {
  fill: black;
  width: 18px;
  height: 18px;
  margin-right: 8px;
}
</style>
