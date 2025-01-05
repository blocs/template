# Github CodespacesでVueを使う時の手順
1. 別ターミナルでサーバー起動 php artisan serve
2. sudo apt-get install npm
3. npm install @vitejs/plugin-vue --save-dev

# コーディング
1. resources/js/app.js
import {createApp} from 'vue';
import App from '../src/App.vue';

createApp(App).mount('#app');

2. resources/src/App.vue
<script setup lang="ts">
import {ref} from "vue";

const name = ref("鈴木一郎");
</script>

<template>
    <h1>こんにちは{{name}}さん!</h1>
</template>

3. テンプレート
<div id="app">
</div>

@vite('resources/js/app.js')

4. npm run dev

# ビルド
1. npm run build
