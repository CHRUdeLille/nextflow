# Nextflow+Singularity inside a singularity container

Nextflow and Singularity help us a lot ! More informations on https://www.nextflow.io and https://singularity.lbl.gov/

## Why this ? Are you schizophrenic ?
We are working in a diagnostic environment and nextflow development is still very active! This is a good thing but we just wanted to be able to run our nextflow scripts in each of the environments corresponding to particular versions of nextflow & singularity.

## Is there any limitation ?
For the moment, you can only use the local executor (https://www.nextflow.io/docs/latest/executor.html#local). We plan to add a slurm client.
