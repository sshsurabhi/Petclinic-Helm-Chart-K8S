# Commands used to create and implement this charts
```bash

    helm create helmchart
    cd helmchart/
    mkdir templates/deployments && templates/misc && templates/services
    mv values.yaml staging-values.yaml
    nano staging-values.yaml 
    nano prod-values.yaml
    nano Chart.yaml 
    cd templates/
    rm _helpers.tpl deployment.yaml hpa.yaml ingress.yaml service.yaml serviceaccount.yaml 
    helm install petclinic petclinic
    helm install petclinic helmchart/petclinic
    helm install petclinic 
    helm install petclinic helmchart
    nano helmchart/templates/misc/secrets.yaml
    nano prod-values.yaml 
    helm install petclinic helmchart -f helmchart/prod-values.yaml 
    helm install petclinic2 helmchart -f helmchart/staging-values.yaml 
```