<template>
    <el-container id="mainPage">
        <el-main>
            <MainPageContent></MainPageContent>
        </el-main>
        <el-footer>
            <Pagination></Pagination>
        </el-footer>
    </el-container>
</template>

<script>
    import MainPageContent from "@/components/mainPage/mainPageContent";
    import Pagination from "@/components/mainPage/pagination";
    export default {
        name: "mainPage",
        components: {
            Pagination,
            MainPageContent,
        }
    }
</script>

<style scoped>

</style>