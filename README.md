# js

评分组件，支持展示评分或者手动评分

使用方法：

1 父组件的json文件中添加组件引用
    "usingComponents": {
            "pictures": "/components/pictures/pictures"
        }
        
 2 wxml文件添加具体实现代码
 <score star="{{star}}" editable="{{true}}" bind:scoreClick="imageClick"></score>
 
 star: 分值，可为小数
 editable: 是否可以手动评分，默认为true
 scoreClick：由于传值使用的triggerEvent，所以需要在父组件监听方法，e.detail即为分值
 imageClick: function (e) {
        this.setData({
            star: e.detail
        })
    }
