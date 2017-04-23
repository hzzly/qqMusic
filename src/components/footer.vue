<template>
    <div class="footer">
        <div class="footer-left">
            <div class="btn_big_prev" @click="_pre"><i class="icon">&#xe601;</i></div>
            <div class="btn_big_play" @click="_play"><i class="icon" style="font-size: 30px;">&#xe607;</i></div>
            <div class="btn_big_next" @click="_next"><i class="icon">&#xe600;</i></div>
        </div>
        <div class="player-music">
            <div class="music">
                <div class="music-info">刚好遇见你 - 李玉刚</div>
                <div class="musin-time">00:00 / 04:26</div>
            </div>
            <div class="progress">
                <div class="player_progress_inner">
                    <div class="player_progress_play"></div>
                </div>
            </div>
        </div>
        <div class="footer-right">
            <div class="play_mod"><i class="icon">&#xe819;</i></div>
            <div class="fav"><i class="icon">&#xe63b;</i></div>
            <div class="down"><i class="icon">&#xe6c0;</i></div>
            <div class="simp_btn"></div>
            <div class="player_voice"><i class="icon" style="font-size: 28px;">&#xe61e;</i></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'footer',
    data() {
        return {

        }
    },
    methods: {
        _pre() {

        },
        _play() {

        },
        _next() {

        }
    }
}
</script>

<style lang="scss" scoped>
.footer {
    height: 11%;
    width: 100%;
    background: 0 0;
    display: flex;
    align-items: flex-start;
    padding: 0 110px;
    box-sizing: border-box;
    color: rgba(225, 225, 225, .9);
    .footer-left {
        display: flex;
        >div {
            margin: 0 25px;
            cursor: pointer;
            &.btn_big_prev,
            &.btn_big_next {
                margin-top: 3px;
            }
            .icon {
                font-size: 24px;
            }
        }
    }
    .player-music {
        flex: 1;
        padding: 0 30px 0 10px;
        .music {
            display: flex;
            justify-content: space-between;
            color: #bdbdbe;
            color: rgba(225, 225, 225, .8);
            font-size: 14px;
            padding: 0 5px;
        }
        .progress {
            height: 8px;
            cursor: pointer;
            overflow: hidden;
            padding: 10px 5px 0 5px;
            .player_progress_inner {
                position: relative;
                height: 2px;
                width: 100%;
                filter: progid:DXImageTransform.Microsoft.gradient(enabled='true', startColorstr='#19FFFFFF', endColorstr='#19FFFFFF');
                background: rgba(255,255,255,.1);
                // .player_progress_load {
                //     width: 100%;
                // }
                .player_progress_play {
                    width: 0%;
                    position: absolute;
                    top: 0;
                    left: 0;
                    height: 2px;
                    filter: progid:DXImageTransform.Microsoft.gradient(enabled='true', startColorstr='#B2FFFFFF', endColorstr='#B2FFFFFF');
                    background: rgba(255,255,255,.7);
                    &::after {
                        content: '';
                        position: absolute;
                        top: -4px;
                        right: -5px;
                        width: 10px;
                        height: 10px;
                        border-radius: 50%;
                        background: #fff;
                        filter: 0;
                    }
                }
            }
        }
    }
    .footer-right {
        display: flex;
        >div {
            margin: 0 10px;
            cursor: pointer;
            .icon {
                font-size: 22px;
            }
        }
    }
    .icon {
        &:hover {
            color: #fff;
        }
    }
}
</style>