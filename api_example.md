> refer to [grafana api](http://docs.grafana.org/http_api/dashboard/)

## use python 
```
url = 'http://192.168.147.130:3000/api/datasources'

#通过页面获取Authorization(非用户名，密码)
header = {
          'Content-Type': 'application/json', 
          'Authorization': 'Bearer eyJrIjoiTks5bUc0dmFsQUdnQnoyTm5uQlFaZW9jSTQwUHIwbXgiLCJuIjoiYWRtaW4iLCJpZCI6MX0=', 
          'Accept': 'application/json'
         }

request = urllib2.Request(url, headers=header)

urllib2.urlopen(request).read()
```

## use curl 

* use api token
```
curl -H "Authorization: Bearer eyJrIjoiTks5bUc0dmFsQUdnQnoyTm5uQlFaZW9jSTQwUHIwbXgiLCJuIjoiYWRtaW4iLCJpZCI6MX0=" http://192.168.147.130:3000/api/datasources
```
* or use password

```
curl http://admin:k7wF8kdfsR59120KGrR1v7r2yMhbLprm3r0W3J7j@192.168.147.130:3000/api/datasources
```
