# Katacoda Checklist templates

Before running this chart please carefully read notes below

## Secrets notes

Create `secrets/` directory inside this chart's directory. 

Direcory structure:

* `jwks.json` with valid rsa jwks json inside
* `db.json` with postgres connect string in the following format
    ```json
    {
        "db_url": "postgres://user:password@host:port/dbname"
    }
    ```

## Important notes on values.yaml

* If you use Istio for ingress routing the `useIstio` parameter should be set to `true`. In this case you need to have ssl certificate created beforehand. The certificate must be stored in `cert-webngt-wildcard` secret in the target namespase you define with the option `-n` when you run `helm install`.

## Run

```bash
helm install -f values.yaml -n checklist checklist .
```
