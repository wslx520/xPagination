## xPagination.js 原生js分页组件

**使用示例**：

    var pagenav = xPagination(pagediv, {
        max:8,
        curr:2,
        size:30,
        pages:22,
        jump:true,
        showSize:[15,30,50],
        onpagination: function  (page, size) {
            console.log('pagediv', page, size)
        }
    })

**支持设置的选项**：

max : 最多同时显示好多页

curr : 当前页码

size : 每页显示多少条，默认15。可以是15,30,50的任一个，如果传为false，则不显示切换每页显示条数的标签

pages : 总好多页。可以不传而只传items，则会由items和size计算出pages

items : 总数据条数。

onpagination : 函数，在页码跳转时触发，此函数执行时会自动传入两个参数：page（当前页）, size（当前页显示条数）

info : 是否显示页码信息，默认true，会加入一个page-text用来显示“共N页，当前是第n页”这样的信息

jump : 是否允许输入页码跳页，默认true,会加入一个页码输入框和确定按钮

prev ：上一页按钮显示的文字，设为false则不显示上一页按钮，下同

next ：下一页按钮显示的文字，同上

last ：末页按钮显示的文字，同上；默认false (2015/12/14 去掉此选项，因为页码算法的改变，页码在任何时候，都会显示第一页和最后一页的页码，用不着用按钮来跳了)

first ：首页按钮显示的文字，同上；默认false (2015/12/14 去掉此选项)

showSize : 是否显示左侧的切换每页多少条，默认false。如果设为true，则会显示当前页码分别乘以1,2,3的size切换；如果设为一个数组如[20,40,80]
，则会以此数组生成对应的size切换

示例请打开`index.html`即可查看