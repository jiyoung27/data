<template>
    <div class="header">
        <ul class="header_button_left">
            <li>Cancel</li>
        </ul>
        <ul class="header_button_right">
            <li>Next</li>
            <!-- step2에서만 보여져야함. 발행버튼을 클릭하면 함수가 실행되도록 -->
        </ul>
        <img src="./assets/logo.png" class="logo" alt="logo" />
    </div>
    <Container :post="post" />
    <div class="footer">
        <ul class="footer_button_plus">
            <li>
                <input type="file" id="file" class="inputfile" />
                <label for="file" class="input_plus">+</label>
            </li>
        </ul>
    </div>
</template>
<script>
import Container from './components/Container.vue';
import postdata from './assets/postdata.js';
export default {
    name: 'App',
    data() {
        return {
            post: postdata
        };
    },
    components: {
        Container: Container
    }
};
</script>
<style>
@import './css/style.css';
</style>
