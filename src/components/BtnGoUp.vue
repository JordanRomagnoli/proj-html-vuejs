<script>
export default {
    data() {
        return {
        }
    }
}
</script>

<template>
    <div class="go-up">
        <a class="go-up-btn border border-dark" href="#top">
            <i class="fa-solid fa-angle-up" style="color: #000000;"></i>
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
    }
}
</style>
