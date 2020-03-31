# Microtask 6:

Execute micro-mordred to obtain data from the study enrich_areas_of_code for any Git repository.

## Solution/Method

Step 1) 

The only think to take care that area of code study is done by git. So in setup.cgf file make sure that area of code study is included.
```
[git]
raw_index = git_chaoss
enriched_index = git_chaoss_enriched
latest-items = false
category = commit
studies = [enrich_areas_of_code:git]
```
Rest all things are same as Microtask 5.

Step 2) 

Execute the micro.py file by following commands

```python3 micro.py --raw --enrich --panels --cfg ./setup.cfg --backends git```
# Demo
![m6.gif](m6.gif)
