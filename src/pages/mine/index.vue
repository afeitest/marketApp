<template>
    <div>
        <view class="banner">
            <view class="bg-color"></view>
            <view class="group">
                <md-icon type="user"></md-icon>
                <p>af_9527</p>
            </view>
        </view>
        <view class="manage-list">
            <md-cell-group>
                <md-cell title="售出记录" thumb="https://tva4.sinaimg.cn/crop.0.0.49.49.50/48e9c764jw1f72iwswntnj201e01e742.jpg?KID=imgbed,tva&Expires=1568607770&ssig=fBMJLfUA9V" is-link></md-cell>
                <md-cell title="意见反馈" thumb="https://tva4.sinaimg.cn/crop.0.0.49.49.50/48e9c764jw1f72iwswntnj201e01e742.jpg?KID=imgbed,tva&Expires=1568607770&ssig=fBMJLfUA9V" is-link></md-cell>
            </md-cell-group>
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
        background-color: #f1f1f1;
    }
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
    .manage-list{
        padding: 0 10px 20px;
        md-cell-group{
            display: block;
            margin-top: 10px;
            font-size: 16px;
        }
    }

</style>
