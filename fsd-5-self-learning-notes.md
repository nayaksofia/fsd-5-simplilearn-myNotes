# Steps Elasticsearch: 
>Step-1:  [Follow this link](https://www.elastic.co/downloads/elasticsearch)

>Step-2 : Download and unzip Elasticsearch.

>Step-3 : Then in terminal window write `cd c:\elasticsearch-7.12.0` 

>Step- 3 : Run in command line `bin/elasticsearch` (or `bin\elasticsearch.bat` on Windows)

>Step- 4 : After that open  the following URL on the browser: `http://localhost:9200/`

Congratulations , You do Set Up  A:  `Single Node Elastic Search`. 

> curl `http://localhost:9200/` or Invoke-RestMethod `http://localhost:9200` with PowerShell

> Refer:  Follow this links: [Install Elasticsearch on Windows](https://www.elastic.co/guide/en/elasticsearch/reference/current/zip-windows.html)

# Set Up Kibana : 

> Step-1: Download and Unzip Kibana

> Step-2: Navigate to that folder in command promt by writing `cd folder-path`

>Step-3: Run `bin/kibana` (or `bin\kibana.bat` on Windows)

>Step-4:  Point your browser at http://localhost:5601 

---

>  Open `config/kibana.yml` in an editor

> Set `elasticsearch.hosts` to point at your Elasticsearch instance


>Step-5: Refer the following link `https://www.elastic.co/guide/en/kibana/current/get-started.html`

 ## Why Kibana Console?

> Elasticsearch has a very rich REST API

> Kibana Console has editor capable and aware of REST API

> It allows for auto-completion and formatting of queries. 

# Set up of Logstash:

> Step-1: Download and unzip Logstash

>Step-2: navigate to the logstatsh path by cusing `cd` command

>Step-3: Then `cd bin`

>Step-4: Then write, `logstash -e "input { stdin{}} output {stdout{}}"

(or)  `Run bin/logstash -f logstash.conf`

>step-5: Now type any text like `Hello` and press `Enter`

>Step-6: Not Exit logstash by writing `Ctrl+ C` command. 

You can execute few more commands:
> `logstash-plugin list`

>`logstash-plugin list 'pager'`

>`logstash-plugin --help`

> `logstash-plugin install logstash-output-email`

> `logstash-plugin update logstash-output-s3`

> Step-2: Prepare a logstash.conf [config file](https://www.elastic.co/guide/en/logstash/current/configuration.html)


```
Input Plugin

Output Plugin

Filter Plugin

Codec Plugin
```

# Exploring Input Plugin

* Plugin:  File
  > File Name: simple1.conf
* JDBC plugin: 
  > File Name: jdbc.conf

# Output Plugin: 


# Sec-1: Lesson-4 Analytics With Elasticsearch


## Types of Aggregation:

* Bucket 
* Metric
* Matrix
  
> Bucket Aggregation 