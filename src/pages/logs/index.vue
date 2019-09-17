<template>
    <div>
        <map
            id="map"
            :longitude="longitude"
            :latitude="latitude"
            scale="14"
            :controls="controls"
            @bindcontroltap="controltap"
            :markers="markers"
            @bindmarkertap="markertap"
            :polyline="polyline"
            @bindregionchange="regionchange"
            show-location
            show-scale
            enable-traffic
            style="width: 100%; height: 100vh;"
        ></map>
    </div>
</template>

<script>

    export default {
        components: {
        },

        data() {
            return {
                longitude: '',
                latitude: '',
                scale: 14,
                // polyline: [{
                //     points: [{
                //         longitude: 113.3245211,
                //         latitude: 23.10229
                //     }, {
                //         longitude: 113.324520,
                //         latitude: 23.21229
                //     }],
                //     color:"#FF0000DD",
                //     width: 2,
                //     dottedLine: true
                // }],
                // controls: [{
                //     id: 1,
                //     iconPath: '/resources/location.png',
                //     position: {
                //         left: 0,
                //         top: 300 - 50,
                //         width: 50,
                //         height: 50
                //     },
                //     clickable: true
                // }]
            }
        },

        computed: {
            markers () {
                return [{
                    iconPath: "/static/tabs/home-active.png",
                    id: 0,
                    latitude: this.latitude,
                    longitude: this.longitude,
                    width: 20,
                    height: 20
                }]
            }
        },

        methods: {
            controltap () {
                console.log('controltap')
            },
            markertap () {
                console.log('markertap')
            },
            regionchange () {
                console.log('regionchange')
            }
        },
        mounted() {
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
        },
        created() {

        }
    }
</script>

<style>
    .log-list {
        display: flex;
        flex-direction: column;
        padding: 40rpx;
    }

    .log-item {
        margin: 10rpx;
    }
</style>
