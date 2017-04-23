<template>
    <div class="header">
        <div class="player_logo">
            <a href="//y.qq.com/#stat=y_new.player.header.logo">
                <img src="../assets/images/player_logo.png" alt="">
            </a>
        </div>
        <div class="mod_player_login">
            <div class="player-login">
                <a href="javascript:;">登录</a>
            </div>
            <div class="player-set">
                <a href="javascript:;">设置</a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'header',
        data() {
            return {

            }
        }
    }
</script>

<style lang="scss" scoped>
    .header {
        height: 70px;
        line-height: 70px;
        width: 100%;
        background: 0 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 55px 0 25px;
        box-sizing: border-box;
        .player_logo {
            width: 78px;
            height: 22px;
            opacity: .3;
            filter: alpha(opacity=30);
            a {
                display: block;
                img {
                    display: block;
                    width: 100%;
                }
            }
            &:hover {
                opacity: 1;
                filter: alpha(opacity=100);
            }
        }
        .mod_player_login {
            display: flex;
            > div {
                a {
                    display: block;
                    padding: 0 10px;
                    font-size: 14px;
                    &:hover {
                        color: #fff;
                    }
                }
            }
        }
    }
</style>