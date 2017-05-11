<template>
    <div id="nav">
        <!--<img src="./assets/logo.png">-->
        <!--<router-view></router-view>-->
        <div class="navigator">
            <!--使用router-link组件导航-->
            <!--通过传入to属性指定链接-->
            <!--<router-link>默认会被渲染成<a>标签-->
            <el-menu theme="dark" :default-active="activeIndex" class="navigator_menu" mode="horizontal" @select="handleSelect">
                <el-menu-item index="1" route="" disabled="">首页</el-menu-item>
                <el-submenu index="2">
                    <template slot="title">总览</template>
                    <el-menu-item index="2-1" route="" disabled="">选项一</el-menu-item>
                    <el-menu-item index="2-1" route="" disabled="">选项二</el-menu-item>
                    <el-menu-item index="2-1" route="" disabled="">选项三</el-menu-item>
                </el-submenu>
                <el-menu-item index="3" route="" disabled=""><a href="hello" target="_blank">订单管理</a> </el-menu-item>
            </el-menu>
        </div>
    </div>
</template>

<script>
    import ElMenu from "../../node_modules/element-ui/packages/menu/src/menu";
    import ElMenuItem from "../../node_modules/element-ui/packages/menu/src/menu-item";
    import ElSubmenu from "../../node_modules/element-ui/packages/menu/src/submenu";
    export default {
        components: {
            ElSubmenu,
            ElMenuItem,
            ElMenu },
        name: 'nav'
    }
</script>
<style>
</style>
