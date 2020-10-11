# Problem Statement
Deploy the model to sagemaker<br/>
<p>Create an API Gateway endpoint that invokes a lambda function.
This lambda function calls the .invoke_endpoint() method with 
any new UFO sighting.  Return the results from the models prediction.</p>
![design](./design_deployment.JPG)

### Steps
1. Sagemaker Notebook: retrain the model.  Then call .deploy().  Jupyternotebook
2. Create a lambda function to invoke_endpoint
3. Create an API gateway to invoke lambda