<script setup>
import { ref } from 'vue'
let aritecles = ref([{ title: "测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE", done: false },{ title: "学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue", done: false }])
defineProps({
    msg: String
})

const count = ref(0)
</script>
<template>
    <div class="textleft" >
        <li  v-for="item in aritecles" style="margin-top:8px;">
            <el-link type="primary" class="textMiddleSize"> {{ item.title }}</el-link>
        </li>
    </div>
</template>

<style scoped>

.textMiddleSize{
    font-size: 18px;
}
</style>

