# cloud-run-function-python-github-action-template

## Run development server

```sh
functions-framework --target hello_get --signature-type=http --port=8080 --debug
```

## Test webhook in local

```sh
ngrok http http://localhost:8080
```

## Deploy to Cloud Run Function

```sh
gcloud beta run deploy $CLOUD_RUN_FUNCTION_NAME \
    --source . \
    --function $TARGET_FUNCTION \
    --base-image <PYTHON_VERSION> \
    --region $REGION \
    --allow-unauthenticated \
    --verbosity=debug
```
