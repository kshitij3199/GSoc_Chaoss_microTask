# Microtask 5:

Execute micro-mordred to collect and enrich data from any Git repository.

# Solution/Method

Step 1) Run ```docker-compose up -d``` to get ElasticSearch, Kibiter and MariaDB. ( as shown in Microtask 4)

Step 2) Make changes in configuration (.cfg) and Projects (.json) file for the Git repository from which data has to be collected and enriched.

Step 3) Execute the micro.py file by following commands

```python3 micro.py --raw --enrich --panels --cfg ./setup.cfg --backends git```

 ```--panels``` Results in creation of dashboards for visulaisation.
 If you dont want it (as not ask in objective, run the command without ```--panels```

# My files
[projects.json](projects.json)

[setup.cfg](setup.cfg)

# Demo

I have used Matrix-react-sdk as a Git repository https://github.com/matrix-org/matrix-react-sdk.git 
(In last year intern, worked on Matrix client based application Riot which uses this)

![m5.gif](m5.gif)
