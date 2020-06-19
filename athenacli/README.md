# athenacli

You can use a docker image for load athenacli.

notice of usage of athenacli on https://www.pgcli.com/

# Usage

You can use athenacli 

```
docker run --rm -it -v <YourHome>:/in -e AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY_ID -e AWS_SECRET_ACCESS_KEY=YOUR_SECRET_ACCESS_KEY -e AWS_DEFAULT_REGION=us-west-2 -e AWS_ATHENA_S3_STAGING_DIR=s3://YOUR_S3_BUCKET/path/to/  dbcliorg/athenacli 
```

If you want to use a specific config

```
docker run --rm -it -v YourDirectoryConfig:/root/.config/athenacli -v <YourHome>:/in -e AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY_ID -e AWS_SECRET_ACCESS_KEY=YOUR_SECRET_ACCESS_KEY -e AWS_DEFAULT_REGION=us-west-2 -e AWS_ATHENA_S3_STAGING_DIR=s3://YOUR_S3_BUCKET/path/to/ dbcliorg/athenacli 
```
