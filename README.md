Tinyurl-wrapper
=============

A wrapper for [tinyurl](http://www.tinyurl.com)
-------

- Based on GAE
- Programmed with Go
- Backend updates transformed urls for every entity regularly and automatically.
- A [jar](https://github.com/XinyueZ/tinyurl4j/tree/master/tinyurl4j/release) will be provided for different client with project [tinyurl4j](https://github.com/XinyueZ/tinyurl4j).


[LICENSE](https://github.com/XinyueZ/tinyurl-wrapper/blob/master/LICENSE)
-------

Param and Return
-------

Param:

Query   |Type       |Comment
--------|---------|---------
q       |string  |Original url which wanna be shorted.

Return:

Var      |Type     |Comment
---------|---------|---------
status   |bool     |Success request or not(false).
q        |string   |Original url which wanna be shorted.
result   |string   |The shorted url by [tinyurl](http://www.tinyurl.com).
stored   |bool     |True if the result is direct from our own database instead of calling [tinyurl](http://www.tinyurl.com).


Example  
-------

Query:

```
https://tinyurl-wrapper.appspot.com/?q=http://www.online.sh.cn
```

Return:

```json
{
  "status": true,
  "q": "http://www.online.sh.cn",
  "result": "http://tinyurl.com/4fwf4",
  "stored": false
}
```
