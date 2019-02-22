<template>
    <div class="hello">
        <router-link to="/page/">卡片 1</router-link>
        <router-link to="/page/child2">卡片 2</router-link>
        <router-link to="/page/child3">卡片 3</router-link>
        <div class="card" style="width: 18rem; margin: auto;">
            <router-view></router-view>
            <!-- <img class="card-img-top" src="http://lorempixel.com/400/200/food/8" alt="Card image cap">
            <div class="card-body">
                <h5 class="card-title">Card title</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
                    content.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div> -->
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            msg: 'welcome to Your Vue.js App'
        }
    }
}
</script>