---
title: Js的三种消息框
date: 2019-05-12 07:09:46
tags:
---
#前言
js消息框类别：警告框、确认框、提示框
<p style="font-size:20px;font-weight:bold;background-color:#000;color:white;">
警告框：alert("文本");</P>
<p style="font-size:20px;font-weight:bold;background-color:#000;color:white;">
确认框：confirm("文本");</P>
<p style="font-size:20px;font-weight:bold;background-color:#000;color:white;">
提示框：prompt("文本","默认值");</P>
<h3 style="color:red;font-size:16px;">
一：confirm使用范例
</h3>
<script type="text/javascript">

       function test(){

        var res = confirm("请选择");

             if(res == true){

               document.write("你点击了确定");

               }else{

     document.write("你点击了取消");

                 }

       }

</script>

<input type="button" onclick="test()" value="confirm">
<h3 style="color:red;font-size:16px;">
使用范例">
二：prompt使用范例：</h3>

<script type="text/javascript">

function test(){

  var name = prompt("名称","jack");

   if(name!=null && name!=""){

          document.write("hello" + name);

      }
    }

</script>

<input type="button" onclick="test()" value="prompt使用范例">
