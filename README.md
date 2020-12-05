# Katacoda Checklist templates

## Run

```bash
helm install -f _values.yaml -n checklist checklist .
```

## Important notes on values.yaml

* If `useIstio` parameter is set to `true` then you need to have ssl certificate created beforehand. The certificate must be stored in `cert-webngt-wildcard` secret in the target namespase you define with the option `-n` when you run `helm install`.
* You must also define a valid value for `jwksSecret` parameter.
