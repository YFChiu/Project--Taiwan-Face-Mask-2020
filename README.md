# Project--Taiwan-Face-Mask-2020
(HDFS, Hive, Bash Script)

## Introduction:
* Taiwan’s mask control policy was implemented in February 2020. Only contracted pharmacies or drugstores, public hospital, and district health office could sell masks on a fixed price. ID was required when inquiring masks in order to track purchasing history.
* This project is aim to track real-time mask stocks over the nation and to optimize best distribution strategy, using docker-compose environment to with Hadoop ecosystem and Spark clusters available for use..
## Data source:
* The open data of the Taiwan National Health Insurance Administration updated the epidemic prevention face mask data every few seconds, showing the availability of mask for sale.
* Scheduling hourly/half hourly/quarterly web scraping from the open data website in March, April and May 2020.
## Project Structure:
### Part 1: Build up Business Data Technology Platform
* Set up CVN68 virtual machine (memory, network)
* Start docker-compose
* Create 4 data scientists Linux user account in machine ‘ds101’ (ds01,ds02,ds03,ds04)
* Create 4 data scientists HDFS home directory from machine ‘adm100’ (/user/{ds01,ds02,ds03,ds04})
### Part 2: Optimize Data Technology Platform
* Set up HDFS Block Replica
* Set up YARN computing resources
* Set up MapReduce computing resources (AppMaster, Map, Reduce)
* Test using teragen, terasort
### Part 3: Data Munging and Injection
* Filter incomplete data
* Merge all datasets
* Save to HDFS (/dataset/twmask)
### Part 4: Data Analysis using Hive
* How many Drugstore were participating in distribution of masks?
* How many adult masks were left in New Taipei City on April 30, 2020?
* How many adult masks were left in Bade District, Taoyuan City at 8am on May 12, 2020?
* How many masks were distributed in Tainan City on May 3, 2020?

