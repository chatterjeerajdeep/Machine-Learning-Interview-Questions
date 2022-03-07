## Data Science Project Life Cycle

A typical data science project life cycle consists of the following steps:

**1. Problem Definition**

### In this step, we must have clarity on the fllowing aspects:
* What is the business requirement?
* Who are the stakeholders?
* What is the simplest solution that adds value to the stakeholders - it may be insights based on descriptive statistics, an analysis that establishes a base line or a mockup dashboard.
* How will value in the project be measured?

**2.Data Investigation and Cleaning**

### This step involves the following processes:
* Gather the data
* Document the data quality
* Clean the data
* Load and visualise the data
* Present initial findings to stakeholders and collect their feedback

### Some technical points here will be:
* calculate various descriptive statistics
* search for outliers
* impute missing values

**3. Minimal Viable Product**

### While developing a prototype, these are the questions to focus on:
* Is the model technically performing better than the baseline
* Is the model able to make a meaningful impact to the underlying business problem?

### What are the modeling approaches to be used?
* Lab validation - to check if the model performs well in a controlled environment
* Wild validation - initial deployment to check how the model performs in the real world. Subjects can be split into 2 groups - test group(impacted by the model) and control group(not impacted by the model)

### How to process the outcomes?
We must ask the following questions:
* Does the model perform better than the baseline model?
* Is it working in the production env?
* Are there any un-intended consequences?

Accordingly, the possible next steps can be:
* Shift the model's focus onto a different topic
* Add more data
* Experiment with different models
* Deploy and enhance the model

**4. Deployment and Enhancement**
**5. Data Science Ops**

This step will involve:
* Monitoring the data - Validating that the real world data coming in is of expected format and of acceptable range
* Monitor Model Performance - Check core metrics 
* Run A/B Tests - Routinely hold-out smaller portions of population as control group to test performance against the running model
* Interpret the model decisions 

