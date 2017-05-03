<template>
    <div class="index">
        <div class="player_bd">
            <div class="mod_songlist_toolbar">
                <ul>
                    <li><i class="icon">&#xe617;</i>收藏</li>
                    <li><i class="icon">&#xe64d;</i>添加到</li>
                    <li><i class="icon">&#xe643;</i>下载</li>
                    <li><i class="icon">&#xe770;</i>删除</li>
                    <li><i class="icon">&#xe6d9;</i>清空列表</li>
                </ul>
            </div>
            <div class="songlist">
                <ul class="songlist_header">
                    <li class="song_edit">
                        <input type="checkbox">
                    </li>
                    <li class="song_name">歌曲</li>
                    <li class="song_author">歌手</li>
                    <li class="song_time">时长</li>
                </ul>
                <ul class="songlist_list">
    
                </ul>
            </div>
        </div>
        <div class="mod_song_info">
    
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<style lang="scss" scoped>
.index {
    height: 100%;
    margin: 0 7.638889%;
    position: relative;
    z-index: 3;
    display: flex;
    .player_bd {
        flex: 1;
        color: #fff;
        opacity: .8;
        top: 3%;
        position: relative;
        filter: alpha(opacity=80);
        .mod_songlist_toolbar {
            margin-bottom: 15px;
            ul {
                display: flex;
                li {
                    min-width: 120px;
                    line-height: 40px;
                    border: 1px solid rgba(255, 255, 255, .2);
                    margin-right: 8px;
                    box-sizing: border-box;
                    text-align: center;
                    cursor: pointer;
                    .icon {
                        margin-right: 5px;
                        vertical-align: bottom;
                    }
                    &:hover {
                        background-color: transparent;
                        color: #fff;
                        opacity: 1;
                        filter: alpha(opacity=100);
                        border-color: #fff;
                        .icon {
                            color: #fff;
                        }
                    }
                }
            }
        }
        .songlist {
            .songlist_header {
                height: 50px;
                line-height: 50px;
                display: flex;
                li {
                    &.song_edit {
                        input[type="checkbox"] {
                            // opacity: 0;
                            // filter: alpha(opacity=0);
                            width: 14px;
                            height: 14px;
                            line-height: 14px;
                            border: 1px solid rgba(225, 225, 225, .2);
                        }
                    }
                    &.song_name {
                        width: 68%;
                        margin-left: 50px;
                    }
                    &.song_author {
                        width: 26%;
                        margin-left: 20px;
                    }
                    &.song_time {
                        width: 80px;
                        margin-left: 20px;
                    }
                }
            }
        }
    }
    .mod_song_info {
        width: 340px;
        margin-left: 150px;
    }
}
</style>