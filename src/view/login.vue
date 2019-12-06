<template>
    <div class="login" v-if="f==false">
        <div class="img">
            <img src="@/assets/1.jpeg" alt="">
        </div>
        <h2>渠道商管理平台</h2>
        <form class="form">
            <select class="sel">
                <option value="">管理员</option>
                <option value="">企业</option>
                <option value="">平台</option>

            </select>
            <input type="text" placeholder="账号名">
            <input type="text" placeholder="账户密码">
            <input type="button" value="登录" class="btn" @click="loginto()">
        </form>
       
            
        
    </div>
     <div v-else class="ok">
            <i class="el-icon-success size animated shake" ></i>
            <p class="msg animated  bounce">登录成功</p>
    </div>
</template>
 

<script>
export default {
    data(){
        return{
            f:false,
            // name:"",
            // password:""
        }
    },
    methods: {
        loginto(){
            // 收集表单数据    ajax---接口---node--数据库查询用户密码是否正确
            // 返回--正确（token） --错误

            // 正确 ---保存token 跳转base页面
            // 错误---当前页面  不跳转
            this.f=true;
            setTimeout(()=>{
                this.$router.push({name:"base"})

            },2000)
        }
    },
}
</script>
<style scoped>
    *{
        margin: 0;
        padding: 0;
    }
    .ok{
       display: flex;
       width: 100px;
       height: 100vh;
       flex-direction: column;
       justify-content: center;
       align-items: center;
       margin: 0 auto;
    }
    .ok p{
        margin-top: 20px;
    }
    .msg{
        text-align: center;
    }
    .size{
        font-size: 100px;
    }
    .login{
        width: 70%;
       
        /* border: 1px solid black; */
        margin: auto;
    }
    h2{
        text-align: center
    }
    .form{
        display: flex;
        flex-direction: column;
    }
    .sel,.form input{
        width: 40%;
        height: 30px;
        margin: 10px auto;
        border-radius: 5px;
        outline: none;
    }
    .btn{
        background: red;
        color: white;
    }
    .img{
        width: 100px;
        height: 100px;
       
        margin: 10px auto;
    }
    img{
        width: 100%;
        height: 100%;
    }
</style>