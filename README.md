Airflow Notes
-----------
# Purpose

To make [Airflow](https://github.com/apache/incubator-airflow) notes and avaible for everyone


# Index

* First example [TBD]
* [List Dags](#list-dags)
* [Run single task](#run-single-task)

## List Dags
#### List all available dags

*Command*
```
AIRFLOW_HOME="$(pwd)" airflow list_dags

```

*Example output*

```
-------------------------------------------------------------------
DAGS
-------------------------------------------------------------------
dag_get_github_profile
```

## Run single task
#### Run Single Airflow Task in a Dag

*Command*

```
AIRFLOW_HOME="$(pwd)" airflow run YOUR_DAG_ID YOUR_TASK_ID RUNING_DATE_TIME
```

*Example*

```
AIRFLOW_HOME="$(pwd)" airflow run dag_get_github_profile slack_notify 2017-09-11T10:20
```

You can see the output in console, and also there is log file in

```
logs/dag_get_github_profile/slack_notify/2017-09-11T10:20
```
