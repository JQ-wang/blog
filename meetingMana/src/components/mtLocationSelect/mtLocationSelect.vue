<style lang="scss">
//区域弹出 Start
.css-curregion{
    color: #308ee3;
}
.css-selector-container {
    .css-mask {
        position: fixed;
        z-index: 501;
        top: 0;
        right: 0;
        left: 0;
        bottom: 0;
        background: rgba(0, 0, 0, 0.6);
    }
    .css-selector-list {
        width: 100%;
        position: absolute;
        z-index: 501;
        top: 50px;
        background-color: #fff;
        max-height: 150px;
        overflow-y: scroll;
        .css-selector-item {
            position: relative;
            padding: 0 22px;
            height: 50px;
            line-height: 50px;
            overflow: hidden;
            white-space: nowrap;
            text-overflow: ellipsis;
            &:after {
                content: " ";
                position: absolute;
                left: 0;
                bottom: 0;
                right: 0;
                height: 1px;
                border-bottom: 1px solid #CCCCCC;
                color: #CCCCCC;
                -webkit-transform-origin: 0 100%;
                transform-origin: 0 100%;
                -webkit-transform: scaleY(0.5);
                transform: scaleY(0.5);
            }
            &.css-curregion {
                color: #308ee3;
            }
        }
    }
}

//区域弹出 End
@mixin placeholder($color) {
     ::-webkit-input-placeholder {
        // WebKit browsers
        color: $color;
    }
     :-moz-placeholder {
        // Mozilla Firefox 4 to 18
        color: $color;
    }
     ::-moz-placeholder {
        // Mozilla Firefox 19+
        color: $color;
    }
     :-ms-input-placeholder {
        // Internet Explorer 10+
        color: $color;
    }
}

@mixin boxshadow($hs, $vs, $blur, $spread, $color:#000) {
    box-shadow: $hs $vs $blur $spread $color;
    -ms-box-shadow: $hs $vs $blur $spread $color;
    -webkit-box-shadow: $hs $vs $blur $spread $color;
    -moz-box-shadow: $hs $vs $blur $spread $color;
    -o-box-shadow: $hs $vs $blur $spread $color;
}

$col9b:#9b9b9b;

@include placeholder(#ccc);
.css-mtlocation-page {
    background-color: #f6f7f8; //主体
    .weui-media-box__title {
        white-space: normal;
    }
    .css-nav-container {
        .weui-navbar__item:active {
            .cov-datepicker {
                background-color: #EDEDED!important;
            }
        }
        .select-btn {
            .css-arrow {
                position: absolute;
                right: 11px;
                top: 19px;
                display: inline-block;
                height: 8px;
                width: 8px;
                border-bottom: 1px solid #98989f;
                border-left: 1px solid #98989f;
                -webkit-transform: rotate(-45deg);
                transform: rotate(-45deg);
                margin-left: 10px;
                margin-bottom: 3px;
            }
            .drop {
                top: 24px;
                -webkit-transform: rotate(135deg);
                transform: rotate(135deg);
                margin-bottom: -2px;
            }
        }
    }
    .css-main-container {
        .css-pageinfo-container {
            position: absolute;
            width: 100%;
            .css-pageinfo {
                background-color: #fff;
                .css-middlescore {
                    border-top: 1px solid #ddd;
                    width: 30px;
                    margin-top: 28px;
                }
                .css-status {
                    padding: 5px 4%;
                    margin-left: 1%;
                    .css-yellow-point {
                        display: inline-block;
                        width: 12px;
                        height: 12px;
                        background-color: #ffba41;
                        border-radius: 50px;
                        margin-right: 5px;
                    }
                    .css-explantime {
                        font-size: 0.5rem;
                        color: $col9b;
                    }
                }

                .css-datetime {
                    padding: 15px 1%;
                    color: $col9b;
                }
                @media (min-width: 340px) {
                    .css-datetime {
                        padding: 15px 2%;
                    }
                }
                @media (min-width: 375px) {
                    .css-datetime {
                        padding: 15px 3%;
                    }
                }
                @media (min-width: 400px) {
                    .css-middlescore {
                        margin-left: 1%;
                        margin-right: 1%;
                    }
                    .css-datetime {
                        padding: 15px 3%;
                    }
                }
            }
        }
        .css-locationdatetime-container {
            padding-top: 55px;
            .css-locationdatetime {
                .css-meetingroom-item {
                    background-color: #fff;
                    height: 80px;
                    .css-meetingroom-name {
                        width: 30%;
                        height: 60px;
                        padding: 0 5%;
                        margin: 10px 0;
                        line-height: 20px;
                        overflow: hidden;
                    }
                    .css-meetingroom-timeline {
                        width: 60%;
                        height: 100%;
                        .css-meetingroom-timeline-box {
                            height: 100%;
                            border-left: 1px solid #e7e7e7;
                            width: 4.55555%;
                            &.room-ordered {
                                background-color: #ffbb41;
                            }
                            &.border-l2 {
                                border-left: 2px solid #e7e7e7;
                            }
                            &.border-r2 {
                                border-right: 2px solid #e7e7e7;
                            }
                        }
                    }
                }
            }
        }
    } //底部bar
    .css-bottombar {
        background-color: #fff;
        &.weui-tabbar:before {
            border: none;
            @include boxshadow(0, -7, 49, 0);
        }
        .css-maxwidth {
            width: 100%;
            .css-inputinco {
                display: block;
                position: absolute;
                left: 5%;
                width: 25px;
                height: 25px;
                background-image: url('../../images/custominput.png');
                background-size: cover;
            }
            .weui-cell__bd .weui-input {
                padding-left: 15%;
                width: 85%;
            }
        }
    }
    .css-nav-container.weui-navbar {
        z-index: 502;
        background-color: #fff;
        .css-select-region {
            padding-left: 8%;
            padding-right: 20%;
            overflow: hidden;
            white-space: nowrap;
            text-overflow: ellipsis;
        }
    }
}
</style>
<template>
    <div class="weui-tab css-mtlocation-page">
        <div class="weui-tab__panel">
            <div class="weui-tab">
                <div class="weui-navbar css-nav-container">
                    <div class="weui-navbar__item select-btn" v-on:click="showtime()">
                        <date-picker :date="startTime" :option="option" :limit="limit"></date-picker>
                        <i class="css-arrow" :class="{drop:isShowtime}"></i>
                    </div>
                    <div class="weui-navbar__item select-btn" v-on:click="showregion()" :class="{'css-curregion':isShowregion}">
                        <div class="css-select-region">{{curRegion}}</div>
                        <i class="css-arrow" :class="{drop:isShowregion}"></i>
                    </div>
                </div>
                <!-- <div v-on:click="showtime()">
                    <date-picker :date="startTime" :option="option" :limit="limit"></date-picker>
                </div> -->
                <div class="weui-tab__panel css-main-container">
                    <section>
                        <div class="css-pageinfo-container">
                            <div class="hr-div"></div>
                            <div class="css-pageinfo clearfix">
                                <div class="css-status fl-l">
                                    <p class="css-notice">
                                        <i class="css-yellow-point"></i>
                                        <span>已预订</span>
                                    </p>
                                    <p class="css-explantime">(每格30分钟)</p>
                                </div>
                                <div class="css-datetime fl-l">
                                    <span>09:00</span>
                                </div>
                                <div class="css-middlescore fl-l"></div>
                                <div class="css-datetime fl-l">
                                    <span>13:00</span>
                                </div>
                                <div class="css-middlescore fl-l"></div>
                                <div class="css-datetime fl-l">
                                    <span>18:00</span>
                                </div>
                            </div>
                        </div>
                    </section>
                    <section>
                        <div class="css-locationdatetime-container">
                            <div class="css-locationdatetime" v-for="meetingromm in ordered" :key="meetingromm">
                                <div class="hr-div"></div>
                                <router-link :to="'/mttimeselect?dddd=11111'" tag="div">
                                    <div class="css-meetingroom-item clearfix">
                                        <div class="css-meetingroom-name fl-l">{{meetingromm.Location}}</div>
                                        <div class="css-meetingroom-timeline fl-l">
                                            <div class="css-meetingroom-timeline-box fl-l" v-for="(ordered,index) in meetingromm.timeorder" :key="ordered" :class="[ordered?'room-ordered':'',index===0?'border-l2':'',index===17?'border-r2':'']"></div>
                                        </div>
                                    </div>
                                </router-link>
                            </div>
                        </div>
                    </section>
                </div>
            </div>
        </div>
        <div class="weui-tabbar css-bottombar">
            <div class="weui-cell css-maxwidth">
                <div class="weui-cell__bd">
                    <i class="css-inputinco"></i>
                    <input class="weui-input" type="text" placeholder="其它地点">
                </div>
            </div>
        </div>
    
        <!-- 区域弹出 End -->
        <div class="css-selector-container" v-if="isShowregion">
            <div class="css-mask" v-on:click="showregion()"></div>
            <div class="css-selector-list">
                <div class="css-selector-item" v-for="item in tabVal" :key="item.Address" v-on:click="regionEvt(item)" :class="{'css-curregion':curRegionId===item.Address}" :curregionid="item.Address">{{item.Name}}</div>
            </div>
        </div>
        <!-- 区域弹出 Start -->
    
        <!-- <psltor :list="tabVal" :curRegionId="curregionId" v-on:listclick="regionEvt()" v-if="isShowregion"></psltor> -->
    </div>
</template>
<script>
import weui from '../../lib/js/weui.min.js';
import moment from 'moment';
import myDatepicker from 'vue-datepicker';
import localdata from '../../js/localdata.js';

export default {
    name: 'mtLocationSelect',
    mounted() {
        for (let i = 0; i < this.initTimenum; i++) {
            this.initTimeitem.push({ value: i })
        }

        this.$http.get('/mt/GetAllPosition').then(response => {
            if (response.status === 200) {
                this.tabVal = response.body.data;
            }
        })
        this.curRegion = 'Webex-云会议室列表';
        this.curRegionId = 'WebexCloudMeeting-room@vipshop.com';
        this.ajaxMtrStatu('/mt/GetRoomsStatus?date=' + this.startTime.time + '&roomListAddress=' + this.curRegionId);

    },
    updated() {
        this.dompadding = document.querySelector('.css-nav-container').offsetHeight;
    },
    data() {
        return {
            startTime: {
                time: moment().format('YYYY-MM-DD')
            },
            endtime: {
                time: ''
            },
            option: {
                type: 'day',
                week: ['一', '二', '三', '四', '五', '六', '日'],
                month: ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月', '九月', '十月', '十一月', '十二月'],
                format: 'YYYY-MM-DD',
                overlayOpacity: 0.5, // 0.5 as default
                dismissible: true // as true as default
            },
            timeoption: {
                type: 'min',
                week: ['Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa', 'Su'],
                month: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
                format: 'YYYY-MM-DD HH:mm'
            },
            multiOption: {
                type: 'multi-day',
                week: ['Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa', 'Su'],
                month: ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'],
                format: "YYYY-MM-DD HH:mm"
            },
            limit: [],

            isCurRegion: false,
            timelist: ['09:00', '09:30', '10:00', '10:30', '11:00', '11:30', '12:00', '12:30', '13:00', '13:30', '14:00', '14:30', '15:00', '15:30', '16:00', '16:30', '17:00', '17:30', '18:00'],
            timeorder: [
                false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false
            ],
            dompadding: 50,//容器padding计算
            isShowregion: false,
            isShowtime: false,
            isNodata: false,
            isShowtab: true,
            initTimenum: 18,//预定格数量
            initTimeitem: [],
            curRegion: '广州广新大厦',
            curRegionId: '',
            tabVal: [
                // { label: '广州广新大厦', value: 0 },
                // { label: '上海上新时代科技大厦', value: 1 },
                // { label: '北京北新科技大厦', value: 2 }
            ],
            ordered:
            [
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // },
                // {
                //     name: '广州-广新2F 巴黎会议室 （18人）', order: [
                //         true, false, false, false, false, true, true, false, false, true, false, false, false, false, true, true, false, false
                //     ]
                // }
            ]
        }
    },
    components: {
        'date-picker': myDatepicker
    },
    methods: {
        //根据会议室Id获取会议室方法
        ajaxMtrStatu(url) {
            this.$http.get(url).then(res => {
                if (res.status === 200) {

                    (function (res, _this) {
                        // let _this = this;
                        //时间区域索引数组
                        let arr = [];
                        let arrNextpage = [];
                        //会议地点数据初始化
                        _this.ordered = res.body.data;
                        //遍历会议数据
                        _this.ordered.forEach((el) => {
                            //取到会议室状态处理
                            arr = [];
                            let objNextpage = {};
                            objNextpage.Id = el.Address;
                            el.RoomStatus.forEach((elrmstatu) => {
                                //空临时对象存储已选中时间索引
                                let obj = {};
                                let timeobg = {}
                                //已选中开始结束时间
                                let st = elrmstatu.Start.split(' ')[1];
                                let ed = elrmstatu.End.split(' ')[1];
                                //存储选中会议室时间格式
                                timeobg.st = st;
                                timeobg.ed = ed;
                                objNextpage.selectedTime = [];
                                objNextpage.selectedTime.push(timeobg);
                                //已选中开始结束时间索引
                                obj.stidx = _this.timelist.indexOf(st.substr(st, st.length - 3));
                                obj.edidx = _this.timelist.indexOf(ed.substr(ed, ed.length - 3));
                                arr.push(obj);
                            }, _this)
                            //存储选中会议室时间
                            arrNextpage.push(objNextpage);
                            localdata.setdata('selectedTime', JSON.stringify(arrNextpage))
                            //时间状态数组
                            _this.timeorder = [
                                false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false
                            ];
                            //遍历选中时间索引匹配选中时间数组
                            arr.forEach((timecheck) => {
                                let sttime = timecheck.stidx;
                                let edtime = timecheck.edidx;

                                _this.timelist.forEach((elinside, idx) => {
                                    if (_this.timeorder[idx]) {
                                        return false;
                                    }
                                    if (idx >= sttime && idx < edtime) {
                                        _this.timeorder[idx] = true;
                                    }
                                }, _this)
                            }, _this)
                            el.timeorder = _this.timeorder;
                        }, _this)
                    })(res, this)
                }
            })
        },
        //时间下拉并处理
        showtime() {
            this.isShowregion = false;
            if (this.isShowtime) {
                this.isShowtime = false;
            } else {
                this.isShowtime = true;
            }
        },
        //处理区域显示及选择
        showregion() {
            // let _this = this;
            this.isShowtime = false;
            if (this.isShowregion) {
                this.isShowregion = false;
            } else {
                this.isShowregion = true;
            }
            // let mtroom = [];
            // this.tabVal.forEach(function (el) {
            //     let obj = {}
            //     obj.label = el.Name;
            //     obj.value = el.Address;
            //     mtroom.push(obj);
            // }, this);
            // weui.picker(mtroom, {
            //     className: 'custom-classname',
            //     defaultValue: [_this.curregion],
            //     onChange: function (result) {
            //         //选中后的处理

            //     },
            //     onConfirm: function (result) {
            //         _this.curregion = result[0].label;
            //         _this.curregionId = result[0].value;
            //         _this.ajaxMtrStatu('/mt/GetRoomsStatus?date=' + _this.startTime.time + '&roomListAddress=' + result[0].value, (res) => {
            //             //时间区域索引数组
            //             let arr = [];
            //             //会议地点数据初始化
            //             _this.ordered = res.body.data;
            //             //遍历会议数据
            //             _this.ordered.forEach((el) => {
            //                 //取到会议室状态处理
            //                 arr = [];
            //                 el.RoomStatus.forEach((elrmstatu) => {
            //                     //空临时对象存储已选中时间索引
            //                     let obj = {};
            //                     //已选中开始结束时间
            //                     let st = elrmstatu.Start.split(' ')[1];
            //                     let ed = elrmstatu.End.split(' ')[1];
            //                     //已选中开始结束时间索引
            //                     obj.stidx = _this.timelist.indexOf(st.substr(st, st.length - 3));
            //                     obj.edidx = _this.timelist.indexOf(ed.substr(ed, ed.length - 3));
            //                     if (obj.stidx.substr(0, obj.stidx.length - 3) > 9 && obj.stidx.substr(0, obj.stidx.length - 3) < 18) {
            //                         arr.push(obj);
            //                     }
            //                 }, _this)
            //                 //时间状态数组
            //                 _this.timeorder = [
            //                     false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false, false
            //                 ];
            //                 //遍历选中时间索引匹配选中时间数组
            //                 arr.forEach((timecheck) => {
            //                     let sttime = timecheck.stidx;
            //                     let edtime = timecheck.edidx;

            //                     _this.timelist.forEach((elinside, idx) => {
            //                         if (_this.timeorder[idx]) {
            //                             return false;
            //                         }
            //                         if (idx >= sttime && idx < edtime) {
            //                             _this.timeorder[idx] = true;
            //                         }
            //                     }, _this)
            //                 }, _this)
            //                 el.timeorder = _this.timeorder;
            //             }, _this)
            //         })
            //     },
            //     onCancel: function () {
            //         _this.isShowregion = false;
            //     },
            //     id: 'pickregion'
            // });
            // document.querySelector('.custom-classname').addEventListener('click', function () {
            //     this.isShowregion = false;
            // })
        },
        regionEvt(item) {
            this.curRegion = item.Name;
            this.curRegionId = item.Address;
            this.ajaxMtrStatu('/mt/GetRoomsStatus?date=' + this.startTime.time + '&roomListAddress=' + item.Address);
            this.showregion();
        },
        totimeselect() {
            this.$router.push({ path: '/mttimeselect' });
        }
    }
} 
</script>
