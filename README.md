## Pré-requisitos
- `kubectl` configurado
- credenciais de uma conta no GCP(Google Cloud Provider) em formato de json nomeado `gcp-credentials.private.json` na raiz do projeto
- 

```
kubectl create secret generic -n vault kms-creds --from-file=../gcp-crede
ntials.private.json
```