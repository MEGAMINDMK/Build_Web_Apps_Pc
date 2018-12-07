# How to create apps
1.download nw from releases<br>
2.move nw folder to C:\Users\urusernamegoeshere\app\nw<br>
3.download node.js<br>
4.after downloading and installing open it and type cd C:\Users\urusernamegoeshere\app\nw\nwjs<br>
5.Now leave the node.js console as it is<br>
6.create a website in html<br>
7.create a file name package.json
add the follwoing to it<br>
<code
{
  
"main"  : "index.html",
  
"name"  : "app",
  
"description": "my first app",
  
"version": "0.1.0",
  
"keywords": [ "console", "gui" ],
  
"window": {
      
"title": "my first app",
	  
"theme": "dark",
      
"icon": "link.png",
	  
"frame" : false,
	  
"toolbar" : false,
	  
"resizable": true,
      
"icon"    : "app/icons/128.png",
      
"width"   : 1000,
     
 "height"  : 600,
      
"position": "center"
  
},
  
"webkit": 
{
    
"plugin": true
  
}

}
</code><br>
8.save it<br>
9.add index.html and package.json to app.zip<br>
10.now rename app.zip to app.nw<br>
11.now move ur app.nw file to C:\Users\urusernamegoeshere\app\nw\nwjs<br>
12.now go back to node.js console and type copy /b nw.exe+app.nw app.exe<br>

an ur apps is ready to clearout some mess make a new folder on desktop and copy the following filenames to new folder<br>

<a href="https://imgbb.com/"><img src="https://imgur.com/MVjD8pp.jpg" alt="bevr" border="0"></a><br>
now share ur app to ur freinds
