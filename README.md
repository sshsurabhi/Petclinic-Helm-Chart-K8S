# Commands used to create and implement this charts
```bash
    helm create helmchart
    cd helmchart/
    mkdir templates/deployments && templates/misc && templates/services
    mv values.yaml staging-values.yaml
    nano staging-values.yaml 
    nano prod-values.yaml
    nano Chart.yaml 
```
+ remove the unnecessary files in the templated folder
```bash
    rm _helpers.tpl deployment.yaml hpa.yaml ingress.yaml service.yaml serviceaccount.yaml 
    helm install petclinic petclinic
    helm install petclinic helmchart/petclinic
    helm install petclinic 
    helm install petclinic helmchart
    nano helmchart/templates/misc/secrets.yaml
    nano prod-values.yaml
```
+ Update the staging-values.yaml, and prod-values.yaml according to the given values.
+ Come out of the helmchart folder, and run the below commands.
```bash
    helm install petclinic helmchart -f helmchart/prod-values.yaml 
    helm install petclinic2 helmchart -f helmchart/staging-values.yaml 
```