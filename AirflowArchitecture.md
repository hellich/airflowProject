# Airflow architecture

## scheduler
- keep track of current time and check if the workflow should be triggered
- retry failed task
- stop workflow and send alerts
- managing logging, metrics and authentication

## Web server

UI with the workflow status and management

## Meta Database
stores :
- workflow executions
- tasks's success and length
- users and roles
- Connections outside of Airflow
- communication layer between components

## Executor

- Get tasks from Scheduler
- Executes tasks
- reports back the state of the task