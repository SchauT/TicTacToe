
<template>
    <div class="footer--container">
        <div class="footer--bottom">
            <div class="container--bottom">
                <div>© TheBrothers, 2022</div>
                <div class="bottom--rs">
                    <nuxt-img src="/images/github-logo.png" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.footer--bottom {
    color: white;
    background-color: #353535;

    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    padding-left: 30px;
}

.container--bottom {
    max-width: 1200px;
    margin: auto;

    display: flex;
    justify-content: space-between;
    padding: 20px 0;
}

.bottom--rs {
    display: inline-block;
    text-decoration: none;
    color: white;
    padding: 0 10px;
    transition: all .2s;
}

.bottom--rs:hover {
    transform: translateY(-2px);
}
</style>