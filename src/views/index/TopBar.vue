<template>
    <div class="top-bar">
       
       <div class="left">
           <span class="iconfont icon-live"></span>
        </div>
       <div class="middle">
           <div class="item" @click="changeTop(0)"><span :class="topIndex===0?'active':''">人才</span></div>
           <div class="item" @click="changeTop(1)"><span :class="topIndex===1?'active':''">雇主</span></div>
           <div class="item" @click="changeTop(2)"><span :class="topIndex===2?'active':''">合伙人</span></div>
           <div class="item" @click="changeTop(3)"><span :class="topIndex===2?'active':''">推荐</span></div>
           <div class="item" @click="changeTop(4)"><span :class="topIndex===2?'active':''">关注</span></div>
    
       </div>

       <div class="right"><span class="iconfont icon-search"></span></div>
    </div>
</template>
<script>
export default {
    name:'topBar',
    data(){
        return{
           topIndex:4 
        }
    },methods:{
        changeTop(index){
            this.topIndex=index;
        }
    }
}
</script>
<style scoped>
.top-bar{
    /* background: #ccc; */
    width: 100%;
    height: 60px;
    line-height: 25px;
    font-size: 18px;
    color: #ccc;
    padding: 20px;
    display: flex;
    box-sizing: border-box;
    position: absolute;
    z-index: 999;
}
.left, .right{
    width: 20%;
}
.iconfont{
    font-size: 24px;
}
.middle{
    width: 60%;
    display: flex;
    justify-items: center;
}
.middle .item{
    flex: 1;
    text-align: center;
}
.middle .item span{
    padding: 10px 0;
}
.middle .item .active{
    color: #e6e926;
    border-bottom: 3px solid;
}
.right{
    text-align: right;
}
</style>