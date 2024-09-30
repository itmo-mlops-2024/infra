FROM ghcr.io/mlflow/mlflow:v2.7.0

RUN apt-get -y update && \
    apt-get -y install python3-dev build-essential pkg-config && \
    pip install --upgrade pip && \
    pip install psycopg2-binary boto3

CMD mlflow server --backend-store-uri $PG_DATABASE --artifacts-destination s3://$AWS_S3_BUCKET_NAME --host 0.0.0.0