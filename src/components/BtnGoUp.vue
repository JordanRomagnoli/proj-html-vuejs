<script>
export default {
    data() {
        return {

        }
    },
    props:{
        Anchor: String,
    }
}
</script>

<template>
    <div class="go-up">
        <a class="go-up-btn" :href="Anchor">
            <i class="fa-solid fa-angle-up"></i>
        </a>
    </div>
</template>

<style lang="scss" scoped>
.go-up {
    position: absolute;
    position: fixed;
    right: 20px;
    bottom: 20px;
    z-index: 1;

    a {
        text-decoration: none;
        display: inline-block;
        width: 40px;
        height: 40px;
        text-align: center;
        line-height: 40px;
        border: 2px solid gray;
        color: gray;
    }
}
</style>
