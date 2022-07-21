## Check my current rate
> Download rate limit 
`ratelimit-limit`, `ratelimit-remaining`

### Set up 
`centos`

~~~ bash
$ yum install -y epel-release
# yum install -y jq
~~~


### Get a token anonymously

~~~ bash
$ TOKEN=$(curl "https://auth.docker.io/token?service=registry.docker.io&scope=repository:ratelimitpreview/test:pull" | jq -r .token) 
~~~


### Get a token with a user account

~~~ bash
$ TOKEN=$(curl --user 'username:password' "https://auth.docker.io/token?service=registry.docker.io&scope=repository:ratelimitpreview/test:pull" | jq -r .token)
~~~

### showing limits 

~~~ bash
$ curl --head -H "Authorization: Bearer $TOKEN" https://registry-1.docker.io/v2/ratelimitpreview/test/manifests/latest
~~~

### Result (return headers)

~~~ text
ratelimit-limit: 100;w=21600
ratelimit-remaining: 76;w=21600
~~~

 이는 21600초 동안 100개의 pull 이 가능하다는 것. (6시간) 그 중, 76번 남은 것.


