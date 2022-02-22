# Airflow Fun
![Airflow Logo](https://upload.wikimedia.org/wikipedia/commons/d/de/AirflowLogo.png)
> Spontaneous hackathon for our team :)
## Airflow installation: 
    https://airflow.apache.org/docs/apache-airflow/stable/start/local.html

## Airflow dags folder config: 
    AIRFLOW__CORE__DAGS_FOLDER=<dags_folder>

## Disable default Airflow DAGs:
    AIRFLOW__CORE__LOAD_EXAMPLES=False

## Airflow Docs
### DAGs
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/dags.html
### Tasks
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/tasks.html
### Operators
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/operators.html
### Sensors
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/sensors.html
### Triggers
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/deferring.html
### XCOMs
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/xcoms.html
### Variables
    https://airflow.apache.org/docs/apache-airflow/stable/concepts/variables.html

## Exercises
### Exercise 1 - Basic ETL
> In this exercise we will create a basic ETL process
#### Instructions
1. Create a DAG which schedules every 10 seconds
2. ***Task1***: Waits for a new file to arrive in input folder
3. ***Task2***: Move all files from input folder to output folder
4. ***Task3***: Print success message in Bash using "echo"

### Exercise 2 - Dungeon Master
> In this exercise we will inspect the Dungeons and Dragons REST API.
#### API Docs:
    https://open5e.com/api-docs
#### REST API Endpoint:
    https://api.open5e.com/
#### SQLITE DB Easy Creation:
    https://sqliteonline.com/
#### Instructions
1. Create a DAG which schedules every 10 seconds
2. ***Task1***: Initialize a new sqlite DB table called Monster that looks like the following example (Without any data):

    | name      | strength | dexterity | constitution | intelligence | wisdom |charisma |
    | --------- | -------- | --------- | ------------ | ------------ | ------ | ------- |
    | Aatxe     | 22       | 12        | 20           | 10           | 14     | 14      |

3. ***Task2***: Waits for D&D API to be available
4. ***Task3***: Request 3 monster details from the D&D API and send it to the next task
5. ***Task4***: Get the monster details from the previous task, then extract only the necessary details about the monsters and save all details into a csv file.
6. ***Task5***: Open the csv file from the previous task and write the monster details into the SQLITE table that you've created in step 2.