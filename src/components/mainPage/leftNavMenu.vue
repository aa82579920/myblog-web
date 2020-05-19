<template>

    <el-row class="tac">

        <el-col :span="24">
            <div class="headImage">
                <div class="block">
                    <el-avatar :size="50" :src="circleUrl" @error="headImageError">
                        <img src="https://cube.elemecdn.com/e/fd/0fc7d20532fdaf769a25683617711png.png"/>
                    </el-avatar>
                </div>
            </div> <!-- 头像 -->
            <div id="name">
                <p>王春杉</p>
            </div>
            <div id="location" >
                <i class="el-icon-location-outline"></i>
                <span slot="title">TianJin, China</span>
            </div>
            <div id="search">
                <el-input size="small" v-model="input" placeholder="请输入内容" prefix-icon="el-icon-search"></el-input>
            </div>

            <el-menu
                    default-active="1"
                    class="leftMenu"
                    @open="handleOpen"
                    @close="handleClose"
                    @select="handleLeftMenuSelect">
                <el-menu-item index="1">
                    <i class="el-icon-s-home"></i>
                    <span slot="title">首页</span>
                </el-menu-item>
                <el-menu-item index="2">
                    <i class="el-icon-menu"></i>
                    <span slot="title">归档</span>
                </el-menu-item>
                <el-menu-item index="3" >
                    <i class="el-icon-document"></i>
                    <span slot="title">分类</span>
                </el-menu-item>
                <el-menu-item index="4">
                    <i class="el-icon-price-tag"></i>
                    <span slot="title">标签</span>
                </el-menu-item>
                <el-menu-item index="5">
                    <i class="el-icon-coordinate"></i>
                    <span slot="title">项目</span>
                </el-menu-item>
                <el-menu-item index="6">
                    <i class="el-icon-s-custom"></i>
                    <span slot="title">关于</span>
                </el-menu-item>
            </el-menu> <!-- 分类标签 -->
        </el-col>

    </el-row>
</template>

<script>
    export default {
        data () {
            return {
                circleUrl: "https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png",
                input: ""
            }
        },
        methods: {
            handleOpen(key, keyPath) {
                console.log(key, keyPath);
            },
            handleClose(key, keyPath) {
                console.log(key, keyPath);
            },
            handleLeftMenuSelect(index, indexPath) {
                console.log(index, indexPath);
            },
            headImageError() {
                return true
            }
        }
    }

</script>

<style>
    .headImage {
        margin-top: 20px;
    }

    #name {
        font-family: "PingFang SC";
        font-size: 20px;
        font-weight: bold;
    }

    #search {
        padding-left: 20px;
        padding-right: 20px;
        margin-top: 10px;
        margin-bottom: 20px;

    }

</style>