<template>
    <my-page title="游戏">
        <div class="common-container">
            <app-list :data="groups" />
        </div>
    </my-page>
</template>

<script>
    export default {
        data () {
            return {
                groups: [
                    {
                        name: '经典',
                        apps: [
                            {
                                name: '2048',
                                desc: '仅限【移动端】',
                                icon: '/static/img/2048.svg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/2048',
                                target: '_blank'
                            },
                            {
                                name: '盖楼',
                                desc: '',
                                icon: '/static/img/tower.png',
                                to: 'xxx',
                                href: 'https://games.yunser.com/tower',
                                target: '_blank'
                            },
                            {
                                name: '俄罗斯方块',
                                desc: '仅限【PC】',
                                icon: '/static/img/tetris.jpg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/tetris',
                                target: '_blank'
                            },
                            {
                                name: '贪食蛇',
                                desc: '仅限【PC】',
                                icon: '/static/img/snake.svg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/snake',
                                target: '_blank'
                            },
                            {
                                name: '扫雷',
                                desc: '仅限【PC】',
                                icon: '/static/img/mine.jpg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/mine',
                                target: '_blank'
                            },
                            {
                                name: '推箱子',
                                desc: '仅限【PC】',
                                icon: '/static/img/game.svg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/push_box',
                                target: '_blank'
                            },
                            {
                                name: '纸牌接龙',
                                desc: '仅限【PC】',
                                icon: '/static/img/game.svg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/jielong',
                                target: '_blank'
                            },
                            {
                                name: '蜘蛛纸牌',
                                desc: '仅限【PC】',
                                icon: '/static/img/game.svg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/spider',
                                target: '_blank'
                            },
                            {
                                name: '跳一跳',
                                desc: '',
                                icon: '/static/img/game.svg',
                                to: 'xxx',
                                href: 'https://jump.yunser.com/jump/jump.html',
                                target: '_blank'
                            },
                            
                        ]
                    },
                    {
                        name: '棋',
                        apps: [
                            {
                                name: '象棋',
                                desc: '',
                                icon: '/static/img/chess.svg',
                                to: 'xxx',
                                href: 'https://demo2.yunser.com/chess/',
                                target: '_blank'
                            },
                            {
                                name: '围棋',
                                desc: '',
                                icon: '/static/img/chess_go.svg',
                                to: 'xxx',
                                href: 'https://demo2.yunser.com/go/',
                                target: '_blank'
                            },
                            {
                                name: '五子棋',
                                desc: '',
                                icon: '/static/img/chess_go.svg',
                                to: 'xxx',
                                href: 'https://demo2.yunser.com/gobang/',
                                target: '_blank'
                            },
                            {
                                name: '飞行棋',
                                desc: '',
                                icon: '/static/img/chess_fly.svg',
                                to: 'xxx',
                                href: 'https://demo2.yunser.com/aeroplane_chess/',
                                target: '_blank'
                            },
                            {
                                name: '井字棋',
                                desc: '',
                                icon: '/static/img/chess_fly.svg',
                                to: 'xxx',
                                href: 'https://games.yunser.com/xox/',
                                target: '_blank'
                            },
                        ]
                    }
                ],
                page: {
                    menu: [
                        {
                            type: 'icon',
                            icon: 'search',
                            href: 'https://search.yunser.com?utm_source=game',
                            target: '_blank',
                            title: '搜索'
                        },
                        {
                            type: 'icon',
                            icon: 'apps',
                            href: 'https://app.yunser.com?utm_source=game',
                            target: '_blank',
                            title: '应用'
                        }
                    ]
                }
            }
        },
        computed: {
        },
        mounted() {
        },
        methods: {
            init() {
            },
            fileChange(e) {
            },
            sizeStr: function (size) {
            }
        }
    }
</script>

<style lang="scss" scoped>
@import '../scss/var';

.tool-list {
    max-width: 840px;
    margin: 0 auto;
    @include clearfix;
    .list-item {
        position: relative;
        float: left;
        width: 260px;
        height: 96px;
        padding: 8px;
        margin: 2px 16px 16px 2px;
        background-color: #fff;
        //border: 1px solid #ccc;
        &:hover {
            background-color: #f9f9f9;
            // box-shadow: 0 3px 10px rgba(0,0,0,.156863), 0 3px 10px rgba(0,0,0,.227451);
            //border-color: #09c;
            .icon {
                display: block;
            }
        }
        &.active {
            border: 1px solid #f00;
        }
    }
    a {
        display: block;
        height: 100%;
        color: #666;
    }
    .img {
        float: left;
        width: 72px;
        height: 72px;
        margin-right: 16px;
        background-color: #fff;
        border: 1px solid #e9e9e9;
        border-radius: 8px;
    }
    .info {
        float: left;
    }
    .text {
        font-size: 18px;
        color: #000;
    }
    .header {
        overflow: hidden;
    }
    .desc {
        max-width: 150px;
        margin-top: 8px;
    }
    .icon-heart {
        display: none;
        position: absolute;
        top: 8px;
        right: 8px;
        &:hover {
            color: #f00;
        }
    }
    .icon-close {
        display: none;
        position: absolute;
        top: 32px;
        right: 8px;
        &:hover {
            color: #f00;
        }
    }
}
@media all and (max-width: 400px){
    .tool-list {
        .list-item {
            width: 100%;
            margin-right: 0;
        }
    }
}
</style>
