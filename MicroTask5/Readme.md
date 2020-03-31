# Microtask 5:

Execute micro-mordred to collect and enrich data from any Git repository.

# Solution/Method

Step 1) Run ```docker-compose up -d``` to get ElasticSearch, Kibiter and MariaDB. ( as shown in Microtask 4)

Step 2) Make changes in configuration (.cfg) and Projects (.json) file for the Git repository from which data has to be collected and enriched.

Step 3) Execute the micro.py file by following commands

```python3 micro.py --raw --enrich --panels --cfg ./setup.cfg --backends git```

# My files

# Demo
