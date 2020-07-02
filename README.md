# Postgres-Backup-Kubernetes-CronJob
This repository contains a helm template of Kubernetes Cron Job which is used for creating backups of Postgres DB.

## Prerequisites
Prerequisites for using this repository are as follows:
* A working instance of Postgres DB.
* Helm. If helm is not installed this template can be manually applied, but the user has to make sure all the jobs are applied correctly, also the configurations in the values.yaml needs to be applied accordingly.
* This container makes use of prebuild Docker image. The required details for building the Docker image can be found in this repository [backup-psql-to-sftp](https://github.com/lalitchilka/backup-psql-to-sftp). 

## Steps to use
* Make sure all the configurations are correct. Eg: Check the values.yaml, and postgresdump-cronjob.yaml
* Run the command helm install postgres-cronJob YourChartName
* This should create a new WorkLoad in your Kubernetes environment. It can be found under WorkLoads -> CronJobs section.
* The cron job will run periodically as per the configuration (schedule: "0 2 * * *") mentioned in the value.yaml.


**Note: Due to privacy policies all the values in the configuration files are dummy value**
