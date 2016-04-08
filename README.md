# redmon
Redis & Sentinel  Monitoring

By default the server listens on endpoint `0.0.0.0:6379`

## Example


### Example url to monitor redis which is running in localhost:6379
`http://localhost:9736/redis/<redis endpoint>`

Ex:
`http://localhost:9736/redis/localhost:6379`



### Example url to monitor redis using sentinel failover
`http://localhost:9736/sentinel/<comma sepeareted sentinel enpoints>/<MaterName>`

***Sentinel Hosts***
* localhost:26379
* localhost:26378

Ex:
`http://localhost:9736/sentinel/localhost:26379,localhost:26378/master`


### Usage
Add the url to any of the http enpoint monitoring tool ex: `pingdom` or `datadog` or `https://github.com/fzaninotto/uptime`

The API will send `200` status in case of success otherwise will respond with `500` status code.
