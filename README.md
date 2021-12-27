<html>
<head>
<meta charset="utf-8">
<title>主页</title>
</head>

<body>
	<ol class="tree">
       <li>
           <label for="folder1" class="folderOne">实验一</label> <input type="checkbox" id="folder1" />  
              <ol>
                <li class="file folderTwo"><a href="sy1-1.html" title="实验1-1">实验1-1</a></li>  
                <li class="file folderTwo"><a href="sy1-2.html" title="实验1-2">实验1-2</a></li>  
                <li class="file folderTwo"><a href="sy1-3.html" title="实验1-3">实验1-3</a></li>
				<li class="file folderTwo"><a href="sy1-4.html" title="实验1-4">实验1-4</a></li>
				<li class="file folderTwo"><a href="sy1-5.html" title="实验1-5">实验1-5</a></li>
				<li class="file folderTwo"><a href="sy1-6.html" title="实验1-6">实验1-6</a></li>
              </ol>
       </li>  
       <li>  
           <label for="folder2"  class="folderOne">实验二</label> <input type="checkbox" id="folder2" />   
           <ol>  
               <li class="file folderTwo"><a href="sy2-1.html" title="实验2-1">实验2-1</a></li> 
               <li class="file folderTwo"><a href="sy2-2.html" title="实验2-2">实验2-2</a></li>
			   <li class="file folderTwo"><a href="sy2-3.html" title="实验2-3">实验2-3</a></li>
			   <li class="file folderTwo"><a href="sy2-4.html" title="实验2-4">实验2-4</a></li>
           </ol>  
       </li>
		<li>
           <label for="folder3" class="folderOne">实验三</label> <input type="checkbox" id="folder3" />  
              <ol>
                <li class="file folderTwo"><a href="sy3-1.html" title="实验3-1">实验3-1</a></li>  
                <li class="file folderTwo"><a href="sy3-2.html" title="实验3-2">实验3-2</a></li>  
                <li class="file folderTwo"><a href="sy3-3.html" title="实验3-3">实验3-3</a></li>
				<li class="file folderTwo"><a href="sy3-4.html" title="实验3-4">实验3-4</a></li>
				<li class="file folderTwo"><a href="sy3-5.html" title="实验3-5">实验3-5</a></li>
				<li class="file folderTwo"><a href="sy3-6.html" title="实验3-6">实验3-6</a></li>
              </ol>
       </li>  
       <li>  
           <label for="folder4"  class="folderOne">实验四</label> <input type="checkbox" id="folder4"/>   
           <ol>  
               <li class="file folderTwo"><a href="sy4-1.html" title="实验4-1">实验4-1</a></li> 
               <li class="file folderTwo"><a href="sy4-2.html" title="实验4-2">实验4-2</a></li> 
           </ol>  
       </li> 
       <li>  
           <label for="folder5"  class="folderOne">实验五</label> <input type="checkbox" id="folder5"/>
		   <ol>  
               <li class="file folderTwo"><a href="sy5.html" title="实验五">实验五</a></li> 
           </ol>
       </li>
	   <li>  
           <label for="folder6"  class="folderOne">实验六</label> <input type="checkbox" id="folder6"/>
		   <ol>  
               <li class="file folderTwo"><a href="sy6.html" title="实验六">实验六</a></li> 
           </ol>
       </li>
	   <li>  
           <label for="folder7"  class="folderOne">实验七</label> <input type="checkbox" id="folder7"/>
		   <ol>  
               <li class="file folderTwo"><a href="sy7-1.html" title="实验7-1">实验7-1</a></li> 
               <li class="file folderTwo"><a href="sy7-2.html" title="实验7-2">实验7-2</a></li> 
           </ol>
       </li>
	<li>  
           <label for="folder8"  class="folderOne"><a href="main.html" title="个人主页">个人主页</a></label> <input type="checkbox" id="folder8"/>
	</li>
   </ol>
<style type="text/css">  
    .tree {margin: 0;padding: 0;background-color:#f2f2f2;overflow: hidden;}  
    /*隐藏input*/
    .tree li input{position: absolute;left: 0;opacity: 0;z-index: 2;cursor: pointer;height: 1em;width:1em;top: 0;}  
    /*所有菜单项设置统一样式*/
    .tree li {position: relative;list-style: none;}   
    /*一级菜单加下边线*/
    .tree>li{border-bottom: 1px solid #d9d9d9;}
    /*给有子菜单的菜单项添加背景图标*/
    .tree li label {max-width:999px;cursor: pointer;display: block;margin:0 0 0 -50px;padding: 15px 10px 15px 70px;background: url(../../images/cp-detail-arrow-b.png) no-repeat right center;background-position:95% 50%;white-space:nowrap;overflow:hidden;text-overflow: ellipsis; }  
    .tree li label:hover,li label:focus{background-color:#a7a7a7;color:#fff;}
    /*清除所有展开的子菜单的display*/
    .tree li input + ol{display: none;}  
    /*当input被选中时，给所有展开的子菜单设置样式*/
    .tree input:checked + ol {padding-left:14px;height: auto;display: block;}  
    .tree input:checked + ol > li { height: auto;}  
    /*末层菜单为A标签，设置样式*/
    .tree li.file a{margin:0 -10px 0 -50px;padding: 15px 20px 15px 70px;text-decoration:none;display: block;color:#333333;white-space:nowrap;overflow:hidden;text-overflow: ellipsis;} 
    .tree li.file a:hover,li.file a:focus{background-color:#a7a7a7;color:#fff;} 
    /*不同层级的菜单字体大小不同*/
    .tree .folderOne{font-size: 18px;}
    .tree .folderTwo{font-size:16px;}
</style>

<script type="text/javascript">
       $(document).ready(function() {
           //每个有子菜单的菜单项添加点击事件
           $(".tree label").click(function(){
               //获取当前菜单旁边input的check状态
               var isChecked = $(this).next("input[type='checkbox']").is(':checked');
               //展开和收齐的不同状态下更换右侧小图标
               if(isChecked){
                   $(this).css(
                       "background-image","url(../images/cp-detail-arrow-b.png)"
                   );
               }else{
                   $(this).css(
                       "background-image","url(../images/cp-detail-arrow-t.png)"
                   );
               }
           });
            
       });
   </script>
</body>
</html>
