##album_manager

###function

####1. albums

参数：

* 路径 path
* 回调函数 callback(err，album_list)

例子：
```js
albums(
    "./",
    function(err,album_list) {
        if (err) {
            console.log(err);
            return;
        }
        console.log(album_list);
    });		
```

####2.create_album(工厂函数)

参数：

* 相册路径 path

返回值：

* Class Album

>类Album(私有)
>>构造函数 Album(path)
>>>属性 name  ， path ， _photos
>>>>方法： photos<br>
>>>>参数： callback(err , photos)

例子：

```js
alb=create_album("../albums/australia2010");
print=console.log;
print(alb.name);
print(alb.path);
print(alb._photos);
alb.photos(function (err,photos) {
	if(err){
		print(err);
		return;
	}
	print(photos);
});
```
