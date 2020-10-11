# Problem Statement
We can used the ground truth dataset (explained, unexplained, or probable)
to predict.
<ul>
<li>Build a model to determine whether newly reported UFO sightings are legitimate or not (explained,
unexplained, or probable).
<li>Model has to be at least 90% accurate
<li>Which algorithm would you choose?
<li>What does our data look like?  Do we need to transform and prepare our data?  Are we missing any values?
<li>How accurate is our model?
</ul>

### Final Results:
<ul>
<li>Model artifact stored into S3
<li>Model validation metrics <br>
  eg:<br>
  multiclass_accuracy: 0.9571 <br>
  macro_recall: 0.95821333 <br>
  macro_precision: 0.91482925
  macro_f_1.000: 0.93460757 
<li>Model error rate
</ul>

### Hint
<ol>
<li>Build a model using XGBoost algorith as a multi-classification problem with researchOutcome as the target attribute.
Goal is to minimize the training and validation error.
<li>Build another model using Linear Learner algorithm as a multi-classification
problem with researchOutcome as the attribute.  Goal is to maximize the
training accuracy (and other metrics
</ol>