# OA前端注意事项

- 外部插件使用时多注意插件提供的参数，不需要自己制造参数或样式来达到效果，尽可能保证功能的单一性    
````
////HTML
<script type="template/text" id="tmpl_create">
  2 <!-- 新建客户 -->
  3 <div class="C-pop y-content-height customer-add-pop">
  4     <form method="get" action="" class="formPop formPop-pro" id="customer_create">
////JS
74                     $(".customer-add-pop").mCustomScrollbar({
75                         set_height:'400'
76                     });
````
上段代码的问题
1. mCustomScrollbar提供设置高度参数，不用再为任何html指定高度
2. html结构中高度应该指定到最上层div而非form
3. form原则上不写渲染性样式
