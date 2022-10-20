# custom-geo-balancing
nginx geo balancer

## Start the stack with docker compose

```bash
$ docker-compose up
```

## Stack

1. 5 caching apps with access to the same resources in 'www' folder:

    URL - http://localhost:81/images/Xbox4.png

    URL - http://localhost:82/images/Xbox4.png

    URL - http://localhost:83/images/Xbox4.png

    URL - http://localhost:84/images/Xbox4.png

    URL - http://localhost:85/images/Xbox4.png




2. Updated https://github.com/sulemanhasib43/nginx_1.16.0_geolite2 as geo balancer:

    URL - http://localhost:90/images/Xbox4.png


By default, IP from Poland redirects to app1,app2, all other redirects to app3, app4. App 5 is backup server.
Response header 'custom' shows information about which app responds, 'iso' shows which location you have.

![image](https://user-images.githubusercontent.com/112312750/196042388-5b07e173-8a66-44db-830e-e952497cab3f.png)






