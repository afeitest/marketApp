<template>
    <div>
        <div class="md-header">销售统计</div>

        <view class="card-group">
            <div class="item">
                <div class="title"><span></span>今日</div>
                <view class="card-row">
                    <view class="card-box">
                        <view class="bar"><p>￥0.00</p><p>今日销售额</p></view>
                    </view>
                    <view class="card-box">
                        <view class="bar"><p>￥0.00</p><p>今日销售额</p></view>
                    </view>
                </view>
            </div>
            <div class="item">
                <div class="title"><span></span>今日</div>
                <view class="card-row">
                    <view class="card-box">
                        <view class="bar"><p>￥0.00</p><p>今日销售额</p></view>
                    </view>
                    <view class="card-box">
                        <view class="bar"><p>￥0.00</p><p>今日销售额</p></view>
                    </view>
                </view>
            </div>
        </view>
    </div>
</template>

<script>
    export default {
        computed: {

        },
        methods: {
        }
    }
</script>

<style lang="scss" rel="stylesheet/scss">
    page {
        padding-top: 66px;
    }
    .card-group {
        .item{
            background-color: #fff;

            .title{
                padding: 0 24px;
                line-height: 40px;
                font-size: 16px;
                border-bottom: 1px solid #efefef;

                span{
                    display: inline-block;
                    width: 6px;
                    height: 6px;
                    vertical-align: top;
                    margin-top: 17px;
                    background-color: #377ff6;
                    border-radius: 3px;
                    margin-right: 10px;
                }
            }

            .card-row{
                padding: 16px 10px;
                @include clearfix();

                .card-box{
                    padding: 0 10px;
                    width: 50%;
                    float: left;
                    .bar{
                        text-align: center;
                        padding: 15px 0;
                        font-size: 12px;
                        line-height: 16px;
                        border-radius: 4px;
                        background-color: #d1e5fc;
                        color: #377ff6;

                        p + p{
                            margin-top: 6px;
                        }
                    }

                    &:last-child{
                        .bar{
                            background-color: #dbefdc;
                            color: #5fb257;
                        }
                    }
                }
            }
        }
    }
</style>
