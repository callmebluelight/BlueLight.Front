<script setup>
import { ref } from 'vue'
let aritecle = ref({
    title: "测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE",
    creater: "bluelight",
    createDate: "2021-08-01",
    details: "11111111111111122222测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE22222222333333333333333344444444444444",
    done: false
})

</script>
<template>
    <div class="textleft">
        <el-container>
            <el-header>{{aritecle.title}}</el-header>
            <el-main>{{aritecle.details}}</el-main>
            <el-footer>{{aritecle.createDate}}</el-footer>
        </el-container>
    </div>
</template>