# databricks-merge-benchmarking

## Overview
Use sample data to test performance on `MERGE` workloads on different Databricks SKUs.

## Disclaimer
It's important to note that this is not production-ready code and is not associated with or endorsed by any employer. The code is intended to be used as-is for experimental and learning purposes only.

## Instructions
1. Replace with your own workspace details in [databricks.yml](./databricks-merge-benchmarking/databricks.yml)
1. Update the job parameters in [resources/run-merges.job.yml](./databricks-merge-benchmarking/resources/run-merges.job.yml)
   1. Note the default parameters work pretty decently (20 target tables of about `5GB`, 50 updates of `100MB` each), but you may need to tune this for your own experimentation
1. Deploy the asset bundle in your workspace
1. Run the created `generate-data-run-benchmarks` job

> [!TIP]
> To get the costs for the jobs accurately:
>   1. You'll need to check [System Tables](https://learn.microsoft.com/en-us/azure/databricks/admin/system-tables/billing)
>   1. For Serverless Jobs, you can just rely on system tables
>   1. For Classic Jobs, you will need to also go to your Cloud Service Provider to get the underlying VM costs
