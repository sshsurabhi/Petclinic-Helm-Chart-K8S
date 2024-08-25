helm create helmchart \n
cd helmchart/ \n
ls
mkdir templates/deployments \n
mkdir templates/misc
mkdir templates/services
ls
mv values.yaml staging-values.yaml
ls
nano staging-values.yaml 
rm staging-values.yaml 
nano staging-values.yaml 
ls
nano prod-values.yaml
ls -a
nano .helmignore 
nano Chart.yaml 
ls templates/
cd templates/
rm _helpers.tpl deployment.yaml hpa.yaml ingress.yaml service.yaml serviceaccount.yaml 
ls
rm -rf tests/
ls
rm NOTES.txt 
cd deployments/
ls
nano api-gateway-deployment.yaml
nano customers-service-deployment.yaml
nano vets-service-deployment.yaml
nano visits-service-deployment.yaml
cd ..
cd misc/
nano config-map.yaml
nano namespace.yaml
nano role.yaml
nano secrets.yaml
cd ..
cd services/
ls
nano api-gateway-ingress.yaml
nano api-gateway-service.yaml
ls
nano customers-service-service.yaml
nano vets-service-service.yaml
nano visits-service-service.yaml
ls
cd helmchart/
ls
cd ..
cd helmchart/
ls
nano Chart.yaml 
helm install petclinic petclinic
cd ..
####
helm install petclinic helmchart/petclinic
helm install petclinic 
helm install petclinic helmchart
nano helmchart/templates/misc/secrets.yaml 
ls
cd helmchart/
ls
nano prod-values.yaml 
cd
helm install petclinic helmchart -f helmchart/prod-values.yaml 
helm install petclinic2 helmchart -f helmchart/staging-values.yaml 
