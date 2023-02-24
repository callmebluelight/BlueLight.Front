<script setup>
import { ref } from 'vue'
let aritecles = ref([{ title: "测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE", describe:"11111111111111122222测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE测试VUE22222222333333333333333344444444444444",done: false },{ title: "学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue",describe:"1111111111111112222222222222333学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue学习vue333333333333344444444444444", done: false }])
defineProps({
    msg: String
})
</script>
<template>
    <div class="textleft" >
        <li  v-for="item in aritecles" style="margin-top:28px;">
            <router-link to="/detail"> {{ item.title }}</router-link>
            <div>
            <span>{{ item.describe }} </span>
        </div>
        </li>
    </div>
</template>