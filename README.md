# Python TDD using CaaS Model
Demo to use Docker Conteiners as Services to do Test Driven Development whit Python

### REQUIREMENTS
Install Docker Engine (Docker Toolbox)

### BUILD
Just run:
```sh
$ docker-compose build
```
This command pull a CentOS image build our container.

### RUN
To start our Dockerized application as a Service just run:
```sh
$ docker-compose up -d
```
### MASIVE TESTS
Place python scripts on "./tests" folder and run 
```sh
$ docker run python_tdd py.test tests/
```
or
```sh
$ docker run python_tdd nosetests tests/
```
To test all scripts on "tests" folder (only recognize those with "test_" prefix) 

### INDIVIDUAL TESTS
Place python scripts on "./tests" folder and run 
 ```sh
$ docker run python_tdd py.test tests/my_test_script.py
```
or
```sh
$ docker run python_tdd nosetests tests/my_test_script.py
```
To test only "my_test_script.py" script