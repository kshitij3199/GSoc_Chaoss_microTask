# Microtask 8:
In your machine, run the tests for ELK within PyCharm. If you succeed, you can try to run the coverage package on the ELK tests and report the details of each file.

Solution/Methods

All the steps are given in [grimoirelab-elk#running-tests](https://github.com/chaoss/grimoirelab-elk#running-tests). Just repeating them.

Step 1)

- update the file [tests.conf](https://github.com/chaoss/grimoirelab-elk/blob/master/tests/tests.conf) in case your ElasticSearch instance isn't available at http://localhost:9200. For example, if you are using the secure edition of elasticsearch, it will be located at https://admin:admin@localhost:9200
- create the databases `test_sh` and `test_projects` in your MySQL instance (e.g., `mysql -u root -e "create database test_sh"`, if you are running mysql in a container use `docker exec -i <container id> mysql -u root -e "create database test_sh"`)
- populate the database `test_projects` with the SQL file [test_projects.sql](https://github.com/chaoss/grimoirelab-elk/blob/master/tests/test_projects.sql) (e.g., `mysql -u root test_projects < tests/test_projects.sql`)

Step 2)

- The tests can be run in combination with the Python package ```coverage```. 

- Install ```coverage``` by following command ```pip3 install coveralls```

Step 3) 

- Move to directory were test are present by ```cd <path-to-ELK>/tests```

Step 4) 
- The full battery of tests can be executed with run_tests.py. However, it is also possible to execute a sub-set of tests by running the single test files (test_* files in the tests folder)
