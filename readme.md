# All Steps 
## Installation 
1. brew install helm

## Create Helm files
1. helm create ui - on the root directory 
    - this will create certain directories like templates, charts
    - from template/ remove tests, ingress, serviceaccount, notes file
2. place your deployment, service, hpa manifests in the templates directory
3. in the value.yaml --> start putting values that changes from your deployment, service, hpa manifests

# Render values into templates
- helm template dev -f ui/values-dev.yaml ./ui/ > dev.yaml
- helm template qa -f ui/values-qa.yaml ./ui/ > qa.yaml
- helm template prod -f ui/values-prod.yaml ./ui/ > prod.yaml