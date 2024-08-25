# Commands used to create and implement this charts
```bash

    helm create helmchart
    cd helmchart/
    mkdir templates/deployments && templates/misc && templates/services
    mv values.yaml staging-values.yaml
    nano staging-values.yaml 
    rm staging-values.yaml 
    nano staging-values.yaml 
    nano prod-values.yaml
    nano Chart.yaml 
    ls templates/
    cd templates/
    rm _helpers.tpl deployment.yaml hpa.yaml ingress.yaml service.yaml serviceaccount.yaml 
    rm -rf tests/
    rm NOTES.txt 
    cd deployments/
    nano api-gateway-deployment.yaml
    nano customers-service-deployment.yaml
    nano vets-service-deployment.yaml
    nano visits-service-deployment.yaml
    nano config-map.yaml
    nano namespace.yaml
    nano role.yaml
    nano secrets.yaml
    nano api-gateway-ingress.yaml
    nano api-gateway-service.yaml
    nano customers-service-service.yaml
    nano vets-service-service.yaml
    nano visits-service-service.yaml
    cd helmchart/
    cd helmchart/
    nano Chart.yaml 
    helm install petclinic petclinic
    helm install petclinic helmchart/petclinic
    helm install petclinic 
    helm install petclinic helmchart
    nano helmchart/templates/misc/secrets.yaml
    nano prod-values.yaml 
    helm install petclinic helmchart -f helmchart/prod-values.yaml 
    helm install petclinic2 helmchart -f helmchart/staging-values.yaml 
```