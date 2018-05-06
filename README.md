# txt2database  
will convert game rule txt to database  

在文件夹128882里面，即阿瓦隆的bgg ID  
有几个比较重要的文件  
avalon.txt  
avalon-conrol.txt  
128882.js  

# avalon.txt
这个文件名字必须跟bgg的英文名一模一样  
这个文件里面是一行行规则，每一行将来对应一个页面  
“|”前面是这个页面标题的名字,  
对应数据库中pageID=128882-1(第一行),  
如果是第二行，则pageID=128882-2  
“|”后面是规则内容  

# avalon-control.txt   
这个文件里面是页面之间关系，与阿鸟你的定义一致,  
我加了上一页，但是本质是一样的  
举例：    
入口|简介-2:配件-3:流程-4:结束-5  
“|”前面是页面标题  
“|”后面是按钮文字和按钮对应的页面  
所以“入口”这个页面有4个按钮,  
第一个按钮上面文字是简介，点击后将跳转到128882-2  
第二个按钮上面文字是配件，点击后将跳转到128882-3（就是前面定义的第三行）  
依次类推  

# 用户提供
现在只要提供  
avalon.txt  
avalon-control.txt  
经过程序运行后，可以在数据库中存储页面结构并生成  
128882.js  
这个文件内容跟阿鸟你提供的模板内容一致    

# 运行命令  
python readrule.py  
python readcontrol.py  
python createjs.py  

# 数据库定义  
请查看库里面的[database.md](./database.md)文件  
  
# TODO  
通过浏览器网页生成  
avalon.txt  
avalon-control.txt  
通过数据库生成  
avalon.txt  
avalon-control.txt  
