
下面是数据库中这两张表每一列的意义的解释  
# raw_control_table  
pageID  
对应一个桌游的一个页面  

textID_1
对应这个页面上面的规则文字

imageID_1  
对应这个页面上面的图片

textID_2
imageID_2
备用，默认一页只显示一行字，一张图  

...

button_1_enable  
button_1_text  
button_1_pageID  
按钮最多支持4个  
button_1_enable代表按钮是否生效，1代表生效，null代表页面不显示这个按钮  
button_1_text代表按钮上面的文字  
button_1_pageID代表按钮点击后会跳转到的页面的pageID  

button_2_enable  
button_2_text  
button_2_pageID  
其它列的功能以此类推  

pageName  
这个是这个pageID对应的也页面的标题  

# raw_text_table  
textID  
代表这个桌游这条规则的编号  

textContent  
规则那一行的内容  

gameID  
游戏bgg编号  

textNum  
默认一页一行，textNum=1,  
如果有多行，textNum可能为2,3,4，  
用来确定多行显示的话，规则的顺序  

pageID  
用来规定这条规则显示在哪个页面上  
