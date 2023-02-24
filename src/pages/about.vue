<template>
    <h1>this is about page</h1>
    <Todolist></Todolist>

    <editor v-model="content" api-key="aabqfn9ljep0mz0n9lh13iozog05osdja4p1clrvkda0igg1" :init="{
        height: 500,
        menubar: false,
        plugins: [
            'advlist autolink lists link image charmap print preview anchor',
            'searchreplace visualblocks code fullscreen',
            'insertdatetime media table paste code help wordcount'
        ],
        toolbar:
            'undo redo | formatselect | bold italic backcolor | \
                   alignleft aligncenter alignright alignjustify | \
                   bullist numlist outdent indent | removeformat | help'
    }" />

    <input type="button" value="test" @click="clear"/>
</template>
    <script setup>
    import Todolist from '../components/Todolist.vue';
    import Editor from '@tinymce/tinymce-vue'
    import { ref } from 'vue'

    let content = ref('');
    
    function clear() {
        alert(content.value);
    }


    </script>
