<template>
    <div>
        <div class="md-header">商品管理</div>
        <view class="manage-group">
            <md-button type="calm" size="small">
                <md-icon type="saoma" size="12" style="display: inline-block"></md-icon>
                新增商品
            </md-button>
        </view>
        <view class="manage-list">
            <md-cell-group>
                <md-cell title="产品名称" is-link extra="操作"></md-cell>
                <md-cell title="条码" extra="123456789"></md-cell>
                <md-cell title="进价" extra="10"></md-cell>
                <md-cell title="售价" extra="20"></md-cell>
                <md-cell title="库存" extra="20"></md-cell>
            </md-cell-group>
            <md-cell-group>
                <md-cell title="产品名称" is-link extra="操作"></md-cell>
                <md-cell title="条码" extra="123456789"></md-cell>
                <md-cell title="进价" extra="10"></md-cell>
                <md-cell title="售价" extra="20"></md-cell>
                <md-cell title="库存" extra="20"></md-cell>
            </md-cell-group>
        </view>

        <view class="manage-from">
            <md-cell-group>
                <md-cell hover-class="none">
                    <md-input label="商品条码" placeholder="请输入商品条码"/>
                </md-cell>
                <md-cell hover-class="none">
                    <md-input label="商品名称" placeholder="请输入商品名称"/>
                </md-cell>
                <md-cell hover-class="none">
                    <md-input label="内含量" placeholder="请输入内含量"/>
                </md-cell>
                <md-cell hover-class="none">
                    <md-input label="箱重量(kg)" placeholder="请输入箱重量"/>
                </md-cell>
            </md-cell-group>
            <md-button type="calm" block>确认</md-button>
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
        background-color: #f1f1f1;
    }
    .manage-group{
        padding:10px 20px;
        background-color: #fff;
        box-shadow: 0 5px 10px rgba(241,241,241,.3);

        .wux-button{
            padding-left: 10px;
            padding-right: 10px;
            border-radius: 30rpx;
        }
    }
    .manage-list,
    .manage-from{
        padding: 0 10px 20px;
        md-cell-group{
            display: block;
            margin-top: 10px;
            font-size: 14px;
        }
    }

</style>
