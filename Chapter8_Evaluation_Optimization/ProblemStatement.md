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

### Hyperparameter Tuning Job:
<ul>
<li> Object Metric: Strategy = Bayesian.  Objecttive metric= validation:object_loss.  Type=minimize
</li>
<li> Early stopping=off. To prevent overfitting</li>
<li> Configuration:
<ul>
<li>feature_dim=22</li>
<li>predictor_type=muticlass_classifier</li>
<li>mini_Batch_size: 500-5000 </li>
<li>learning_rate= .0001 - 1.0 </li>
<li>wd = .0001-1.0 </li>
<li>l1 = .0001-1.0 </li>
<li>num_class = 3 </li>
</ul>
</li>
</ul>

### Data Input and Output:
<ul>
<li>Create 2 channels: train and validation with the respective input mode (pipe or file),
and the S3 locations.</li>
<li>Specify Output location</li>
</ul>

### Resource Configuration and Limit
<ul>
<li> Resource Configuration: instance type</li>
<li> Resource Limits:
  <ul>
  <li>Maximum training jobs: 50
  <li>Maximum parallel training jobs: 5 (Note:10 is max. larger would cause the parallel jobs don't know other training jobs outcome)
  <li>Max duration per training job: 5 min
  </ul>
  </li>
 </ul>

### Best Training Job tab
Select the best training job parameters and use the jupyter notebook to train the model