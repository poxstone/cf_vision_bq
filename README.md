# Cloud Storage + cloudfunctions + BigQuery

## APIS
- Authorize: Vision API, CloudStorage JSON

## Deploy
```bash
export PROJECT='<PROJECT>';
export BUCKET='<BUCKET>';
gcloud functions deploy "event_trigger" --runtime "python37" --trigger-resource "$BUCKET" --trigger-event "google.storage.object.finalize" --project "$PROJECT";
```


## bigquery
- **Dataset name**: "storage_image"
- **Table name**: "labels"
- **Schema**: file:STRING,labels:STRING

