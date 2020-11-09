# Day 28 - Threat Hunting with ELK Stack
11/11/20

* [AWS: What is the ELK stack?](https://aws.amazon.com/elasticsearch-service/the-elk-stack/)
* [SQRLL: A Framework for Cyber Threat Hunting PDF](https://www.threathunting.net/files/framework-for-threat-hunting-whitepaper.pdf)</br>
What is hunting?</br>
HMM</br>
Hunting Loop</br>
Hunt Matrix</br>

"he ELK stack gives you the ability to aggregate logs from all your systems and applications, analyze these logs, and create visualizations for application and infrastructure monitoring, faster troubleshooting, security analytics, and more."

**E = Elasticsearch**</br>
Elasticsearch is an open-source, RESTful, distributed search and analytics engine built on Apache Lucene. Support for various languages, high performance, and schema-free JSON documents makes Elasticsearch an ideal choice for various log analytics and search use cases.

**L = Logstash**</br>
Logstash is an open-source data ingestion tool that allows you to collect data from a variety of sources, transform it, and send it to your desired destination. With pre-built filters and support for over 200 plugins, Logstash allows users to easily ingest data regardless of the data source or type. 

**K = Kibana**</br>
Kibana is an open-source data visualization and exploration tool for reviewing logs and events. Kibana offers easy-to-use, interactive charts, pre-built aggregations and filters, and geospatial support and making it the preferred choice for visualizing data stored in Elasticsearch.

Automated, scalable, secure.

***What is hunting?***</br>
"Hunting consists of manual or machine-assisted techniques, as opposed to relying only on
automated systems like SIEMs." "In fact, one of the chief goals of hunting should be to improve automated detection by prototyping new ways to detect malicious activity and then turning those prototypes into effective new automations."

***HMM***</br>
"There are a number of factors to consider when judging an organization’s hunting ability, including:"
* The quantity and quality of the data they collect
* In what ways they can visualize and analyze various types of data
* What kinds of automated analytic they can apply to data to enhance analyst insights

Five levels of organizational hunting capability:
1. HM0 - Initial (not capable of hunting)
2. HM1 - MINIMAL 
3. HM2 - PROCEDURAL (most common level)
4. HM3 - INNOVATIVE 
5. HM4 - LEADING (any successful hunting process will be operationalized and turned into
automated detection)

***The Hunting Loop***</br>
"To avoid one-off, potentially ineffective “hunting trips,” it is important for your team to implement a formal cyber hunting process." 
Four steps:</br>
1. Hyopothesis generation - crafting increasingly more dynamic questions, and
moving from manual hypothesis creation to automatic generation via risk scoring analytics
2. Tool & Technique enabled investigation - o follow up on hypotheses is dependent on moving from
using simple searches and histograms to using tools with advanced visualizations and graph
search capabilities.
3. Pattern and TTP discovery - expanding the kinds of Indicators of compromise (IoCs) you can collect from the Pyramid of Pain.
4. Automated Analytics - moving from simple analytics such as
stack counting, to advanced and automated analytics powered by machine learning, and moving
from repeated searches to feeding gathered information back into your automated detection
systems.

"The hunting loop is a simple but effective process that can radically enhance an organization’s
network defense. It is most effective when it is used together with traditional security systems,
complementing detection efforts that most organizations already have in place. The ultimate objective of a hunting team should always be to get through the loop as efficiently as possible."

***The Hunt Matrix***</br>
"Data collection from HM0 to HM4 matures in a linear way,
from collecting little to no data to collecting many different types of data from throughout your IT
environment." 

