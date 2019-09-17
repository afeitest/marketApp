<template>
    <div>
        <view class="banner">
            <view class="bg-color"></view>
            <view class="group">
                <md-icon type="saoma"></md-icon>
            </view>
        </view>
        <view class="sm-group">
            <view class="item" style="background-color: #377ff6">
                <h2>进货</h2>
                <p>扫一扫商品条码</p>
                <md-icon type="saoma" size="24"></md-icon>
            </view>
            <view class="item" style="background-color: #e38139">
                <h2>售出</h2>
                <p>扫一扫商品条码</p>
                <md-icon type="saoma" size="24"></md-icon>
            </view>
        </view>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            }
        },

        components: {
        },
        onPullDownRefresh () {
            // 下拉刷新回调
            this.onRefresh()
        },
        methods: {
            onRefresh: function() {
                setTimeout(() => {
                    // 结束下拉刷新
                    wx.stopPullDownRefresh()
                },3e3)
            },
            getLoaction () {
                let vm = this
                wx.getLocation({
                    type: 'gcj02',
                    success: function (res) {
                        console.log(res)
                        vm.latitude = res.latitude
                        vm.longitude = res.longitude
                        wx.openLocation({//​使用微信内置地图查看位置。
                            latitude: res.latitude,//要去的纬度-地址
                            longitude: res.longitude,//要去的经度-地址
                            // name: "O'MALL华侨城商业中心",
                            // address: '华侨城商业中心'
                        })
                    }
                })
            }
        },
        mounted() {
            document.getElementsByTagName('page').className = 'fixed';
        }
    }
</script>

<style lang="scss" rel="stylesheet/scss">
    .banner{
        position: relative;
        height: 480rpx;
        overflow: hidden;
        .bg-color{
            position: absolute;
            z-index: -1;
            left: -50%;
            bottom: 0;
            width: 200%;
            height: 200%;
            border-radius: 0 0 100% 100%;
            background-image:linear-gradient(135deg, #469cf7 30%, #76daa3 70%);
        }
        .group{
            text-align: center;
            color: #fff;
            padding-top: 100px;
        }
    }

    .sm-group{
        position: relative;
        padding: 0 20px;
        margin:20px auto 0;
        .item{
            position: relative;
            display: block;
            margin-top: 20px;
            border-radius: 5px;
            overflow: hidden;
            padding: 16px;
            color: #fff;
            background-color: #377ff6;
            box-shadow: 0 5px 10px rgba(0,0,0,.2);
            &:after{
                display: block;
                content: "";
                width: 100%;
                height: 100%;
                position: absolute;
                left: 0;
                bottom: 0;
                pointer-events: none;
                background-size: 100% auto;
                background-repeat: no-repeat;
                background-position: center bottom;
                background-image: url("../../../static/images/sm_bg.png");
            }

            md-icon{
                position: absolute;
                right: 16px;
                top: 16px;
            }
            h2{
                font-size: 20px;
            }
            p{
                font-size: 14px;
                margin-top: 10px;
            }
        }

    }
    .page-section{
        width: 100%;
    }

</style>
