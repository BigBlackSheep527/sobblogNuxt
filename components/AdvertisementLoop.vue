<template>
    <div style="background: #FFFFFF;height: 270px; margin-top: 0" >
      <h3 style="margin-top: 0">
        <svg t="1612748343177" class="icon" viewBox="0 0 1408 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="1905" width="200" height="200"><path d="M1306.88 867.328H40.448A40.576 40.576 0 0 1 0 826.88V181.376A181.888 181.888 0 0 1 181.376 0h984.576a181.888 181.888 0 0 1 181.376 181.376V826.88a40.576 40.576 0 0 1-40.448 40.448z m0 139.584H40.448A40.576 40.576 0 0 1 0 966.464c0-22.272 18.24-40.448 40.448-40.448H1306.24c22.208 0 40.448 18.176 40.448 40.448a39.552 39.552 0 0 1-39.808 40.448zM321.984 607.36c0 1.28-0.64 2.688-1.984 4.672v15.552c1.344 23.616 14.848 35.072 39.808 35.072 20.224 0 34.368-8.768 41.792-26.304l17.536-52.608h155.072l15.488 52.608c6.08 17.536 19.584 26.24 41.856 26.24 24.96 0 38.4-10.752 39.744-32.96a95.232 95.232 0 0 1-4.672-22.272L556.672 301.888c-12.8-28.992-33.728-44.544-61.376-45.888-28.992 1.344-49.216 16.832-59.328 45.888L322.048 607.36zM496 343.68l52.608 162.56H443.392l52.608-162.56z m229.952 277.12c0 26.304 14.848 39.808 43.84 41.152h96.448c122.048-6.08 186.112-70.784 193.536-195.584-5.44-130.112-71.488-198.208-197.632-204.288h-94.4c-26.24 2.688-40.448 16.832-41.792 41.792V620.8z m83.584-281.856h50.56c72.832 1.344 110.656 43.136 112 125.44-4.096 78.848-39.168 119.36-105.216 120.704h-57.344V338.944z" p-id="1906"></path></svg>
        <span>广告</span>
        <span class="line"></span>
      </h3>
      <div v-if="isShow" style="position: relative; top:-35px; padding: 5px">
      <el-carousel :interval="3000" arrow="always" id="adv">
        <el-carousel-item v-for="(item,index) in loop" :key="index">
          <svg style="width: 20px;height: 20px; position: relative; top:25px; left: 200px" @click="isShow=false" t="1612750316486" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3886" width="200" height="200"><path d="M29.824 512c0-266.688 216-482.688 482.176-482.688a482.304 482.304 0 0 1 482.176 482.176V512A481.664 481.664 0 0 1 512 994.176 481.984 481.984 0 0 1 29.824 512z m514.432 0L712.64 343.616a21.888 21.888 0 0 0 0-31.232l-1.024-1.024a21.888 21.888 0 0 0-31.232 0L512 480.32 343.616 311.36a21.888 21.888 0 0 0-31.232 0l-1.024 1.024a21.888 21.888 0 0 0 0 31.232l168.384 168.896L311.36 680.896a21.888 21.888 0 0 0 0 31.232l1.024 1.024a21.888 21.888 0 0 0 31.232 0L512 544.768l168.384 168.384a21.888 21.888 0 0 0 31.232 0l1.024-1.024a21.888 21.888 0 0 0 0-31.232L544.256 512z" fill="#cdcdcd" p-id="3887"></path></svg>
          <a :href="item.coupon_click_url" > <img :src="item.pict_url+'_320x320xzq90.jpg_.webp'"> </a>
        </el-carousel-item>
      </el-carousel>
      </div>
      <div id="restart" style="" v-else>
        <svg style="position: relative;left: 40px;top: 20px; width: 150px;height: 150px" @click="isShow=true" t="1612752716629" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4741" width="200" height="200"><path d="M716.8 290.133333c-110.933333-102.4-281.6-106.666667-396.8-12.8S170.666667 537.6 247.466667 665.6c59.733333 106.666667 179.2 166.4 302.933333 149.333333s221.866667-102.4 256-221.866666c8.533333-34.133333 42.666667-51.2 76.8-42.666667 34.133333 8.533333 51.2 42.666667 42.666667 76.8-68.266667 226.133333-302.933333 354.133333-524.8 290.133333C174.933333 853.333333 42.666667 618.666667 106.666667 392.533333c42.666667-145.066667 153.6-256 298.666666-298.666666s298.666667 0 405.333334 102.4l81.066666-81.066667c8.533333-8.533333 21.333333-12.8 34.133334-8.533333 4.266667 12.8 12.8 21.333333 12.8 34.133333v264.533333c0 17.066667-12.8 29.866667-29.866667 29.866667h-260.266667c-12.8 0-25.6-8.533333-29.866666-17.066667s0-25.6 8.533333-34.133333l89.6-93.866667z" p-id="4742" fill="#dbdbdb"></path></svg>
      </div>
    </div>
</template>
<script>
  import * as api from '../api/api'
  export default {
    data(){
      return{
        loop:[],
        isShow: false
      }
    },
    methods:{
      getTaobaoLoop(){
        api.getTaobaoLoop().then(result=>{
          if(result.code===10000){
            this.loop=result.data.tbk_dg_optimus_material_response.result_list.map_data;
            console.log(this.loop.pict_url)
          }else {
            this.$message.error(result.message)
          }
        })
      },
      clear(){
        document.getElementById('adv').style.display='none'
      }
    },
    mounted() {
      this.getTaobaoLoop();
    }

  }
</script>


<style >
   img{
    width:230px;
    height: 210px;
   border-radius: 5%;
  }
  .el-carousel__indicator--horizontal {
    display: none;
    padding: 12px 4px;
  }
  .el-carousel__container {
    position: relative;
    height: 231px;
  }
  h3 .line {
    width: 10px;
    height: 1px;
    background: #54b5db;
    margin-left: 12px;
  }
  h3 .icon {
    fill: black;
    width: 18px;
    height: 18px;
    margin-right: 8px;
  }
  h3 {
    display: flex;
    align-items: center;
    border-bottom: 1px solid #EBEEF5;
    font-size: 16px;
    font-weight: 500;
    height: 45px;
    line-height: 45px;
    padding: 0 15px;
    color: black;
  }
</style>
