## Helm Chart Deployment

This section provides the instructions for deploying the PetClinic application using Helm charts, based on the infrastructure previously provisioned in AWS.

### Steps to Create and Deploy the Helm Chart

1. **Create a New Helm Chart:**
   ```bash
   helm create helmchart

2. **Navigate to the Helm Chart Directory:**
    ```bash
    cd helmchart/

3. **Set Up the Template Structure:**
Create necessary directories for deployments, miscellaneous templates, and services:
    ```bash
    mkdir templates/deployments && templates/misc && templates/services

4. **Modify the** values.yaml:
    ```bash
    mv values.yaml staging-values.yaml
    nano staging-values.yaml
    nano prod-values.yaml

5. **Edit the Chart Configuration:**
Open and modify the Chart.yaml as needed:
    ```bash
    nano Chart.yaml

6. **Remove Unnecessary Default Files:**
Clean up the default templates that were created with the chart:
    ```bash
    rm _helpers.tpl deployment.yaml hpa.yaml ingress.yaml service.yaml serviceaccount.yaml

7. **Install the PetClinic Application:**
Use Helm to install the PetClinic application to your Kubernetes cluster:
    ```bash
    helm install petclinic petclinic

The following are additional commands to ensure the application is installed correctly using the Helm chart:
    ```bash
    helm install petclinic helmchart/petclinic
    helm install petclinic helmchart

8. **Manage Secrets and Configuration:**
Update or create secrets for your application:
    ```bash
    nano helmchart/templates/misc/secrets.yaml
    nano prod-values.yaml
9. **Deploy Using Production Values:**
Install the PetClinic application using the production values configuration:
    ```bash
    helm install petclinic helmchart -f helmchart/prod-values.yaml 

10. **Deploy Using Staging Values:**
You can also deploy a different instance of the application using a staging configuration:
    ```bash
    helm install petclinic2 helmchart -f helmchart/staging-values.yaml 

## Summary
This deployment method enables you to leverage Helm for managing the PetClinic application, ensuring a consistent and simplified deployment process that integrates with the AWS infrastructure created with Terraform. Adjust the configuration values according to your environment and application requirements.


Feel free to modify any part of this section to better align with your actual commands, directory structures, or naming conventions used in your project. You can also add any additional details or notes that might be useful for users who are following the instructions.

---

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