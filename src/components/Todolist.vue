<template>
    <div>{{ title1 }}
        <input type="text" v-model="title" @keydown.enter="addTodo" />
        <button v-if="active<all" @click="clear">清理</button>
        <ul v-if="todos.length">
            <li v-for="todo in todos">
                <input type="checkbox" v-model="todo.done" />
                <span :class="{done:todo.done}">
                {{todo.title}}
                </span>
            </li>
        </ul>
        <div v-else>暂无数据</div>
        <div>
            全选<input type="checkbox" v-model="allDone" />
            <span>{{active}}/{{all}}</span>
        </div>
    </div>
</template>
<script setup>
import { computed } from '@vue/reactivity';
import { ref } from 'vue'

defineProps(['title1'])

let title = ref('');
let todos = ref([{title:"吃饭",done:false}])
const addTodo = () => {
    todos.value.push({title:title.value,done:false})
    title.value = ''
}
function clear(){
    todos.value = todos.value.filter(todo=>!todo.done)
}
let active=computed(()=>todos.value.filter(todo=>!todo.done).length)
let all=computed(()=>todos.value.length)
let allDone = computed({
    get(){
        return active.value === 0
    },
    set(val){
        todos.value.forEach(todo=>todo.done=val)
    }
})
</script>