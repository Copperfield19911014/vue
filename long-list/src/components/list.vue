<template>
    <div class="div_body">
        <div class="div_container">
            <div ref="phantom" class="phantom" ></div>
            <table class="table">
                <!-- <tr>
                    <th>序号</th>
                    <th>姓名</th>
                    <th>年龄</th>
                    <th>性别</th>
                    <th>生日</th>
                    <th>身份</th>
                </tr> -->
                <tr class="tr" :key="index" v-for="(item, index) in list">
                    <td>序号:{{item.index}}</td>
                    <td>姓名:{{item.index}}</td>
                    <td>年龄:{{item.index}}</td>
                    <td>性别:{{item.index}}</td>
                    <td>生日:{{item.index}}</td>
                    <td>身份:{{item.index}}</td>
                    <td>序号:{{item.index}}</td>
                    <td>姓名:{{item.index}}</td>
                    <td>年龄:{{item.index}}</td>
                    <td>性别:{{item.index}}</td>
                    <td>生日:{{item.index}}</td>
                    <td>身份:{{item.index}}</td>
                    
                </tr>
            </table>
        </div>
        
    </div>
    
</template>
<script>

export default{
    data() {
        return {
            list :[],
            showList: [],
            startIndex: 0,
            endIndex: 10
        }
    },
    created(){
        let _this = this
        let num = 1000
        for(let i = 0;i < num;i++){
            _this.list.push({
                index: i
            })
        }
        this.showList = this.list.splice(this.startIndex, this.endIndex)
        
    },
    mounted(){
        this.setPhantomHeight()
    },
    methods: {
        setPhantomHeight(){
            this.$refs.phantom.style.height = 60 * this.list.length + 'px'
            console.log(this.$refs.phantom.clientHeight)

        }
    }
}
</script>
<style >
    .div_body{
        width: 90%;
        margin: auto;
        height:600px;
        border: solid 3px #ccc;
    }
    .div_container{
        position: relative;
        width: 100%;
        height: 100%;
        overflow: auto;
    }
    .phantom{
        border: solid 2px red;
    }
    .table{
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
    }
    .tr{
        height: 60px !important;
    }
</style>
