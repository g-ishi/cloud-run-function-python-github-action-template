# calc-nutrient-function

## Run development server

```sh
functions-framework --target patch_nutrients --signature-type=http --port=8080 --debug
```

## Test webhook in local

```sh
ngrok http http://localhost:8080
```

## Deploy to Cloud Run Function

```sh
gcloud beta run deploy calc-nutrient-function \
    --source . \
    --function patch_nutrients \
    --base-image python312 \
    --region asia-northeast3 \
    --allow-unauthenticated
```
# cloud-run-function-python-github-action-template
