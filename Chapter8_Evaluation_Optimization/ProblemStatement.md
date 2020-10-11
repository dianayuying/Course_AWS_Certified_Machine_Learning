# Problem Statement
<ul>
<li> Tune our model to find the most optimzed model for our problem</li>
<li>Determine if the model is less accurate, more accurate, or about the same</li>
<li>What objective metric would you want to monitor to ensure this?  How do you plan on measuring success?</li>
<li>Which hyperparameters need to be tuned?  What combination of hyper parameters need to be used?</li>
<li>How much faster was training time improved?</li>
</ul>

### Hint:
Create a sagemaker hyperparameter tuning job with different ranges 
of values for hyperparameters to find the best 
configuration to minimize the ```validation:objective_loss``` metric.
