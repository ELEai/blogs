# How to Deploy a Machine Learning Risk Classification Model with Amazon AWS

Intro paragraph


## The Benefits of using Amazon SageMaker Model Endpoints

There are many benefits of using Amazon SageMaker to manage your model endpoints...

1. The service is fully managed, meaning Amazon will take care of a number of tasks associated with provisioning a model into production and optimizing the required infracture according to your needs. 
 - [__Inference Pipelines__](https://docs.aws.amazon.com/sagemaker/latest/): Models are most often not standalone entities, but ensembles and stacks of data transformed multiple times over before the final result is infered. SageMaker  provides an easy way to orchistrate multiple inferences and transformations into a single pipeline.
 - [__Auto Scaling__](https://docs.aws.amazon.com/sagemaker/latest/dg/endpoint-auto-scaling.html): Set a CloudWatch alarm to trigger additional computing power by spinning up additional EC2 instances when you get a spike in model inference calls. This helps if you are interested in making real-time inferences and you have an unpredictible request load. 
 - [__Elastic Inferece (EI)__](https://docs.aws.amazon.com/sagemaker/latest/dg/ei.html): Do you have a computationally heavy model inference but don't like the high cost of hosting your endpoint on a GPU? Amazon EI is a service that will speed up the throughput of your deep learning models by provisioning an "accelerator" compute resource at the time the model is called. In many cases you can ditch the GPU.
 - [__Neo__](https://docs.aws.amazon.com/sagemaker/latest/dg/neo.html): Neo can optimize your model across TensorFlow, Apache MXNet, PyTorch, ONNX, and XGBoost for deployment on ARM, Intel, and Nvidia processors. Train your model once and use it anywhere. 
 
2. Using SageMaker promotes transparancy and collaboration by centralizing model development activities on a single platform. If you are a manager or owner and you are interested in monitoring your Data Science team's activities and utilization, then using SageMaker in conjunction with IAM, CloudWatch and CloudTrail can give you insights into what data is being accessed, who (or what) is accessing that data, and how much these activities costing. 

If you are a Data Scientist, you will appreciate how easy it is to organize, annotate, and share your work with colleagues and managers by using the built-in jupyter notebooks. The environment you configure in the notebook stays in the cloud, making it easy to pick up where you left off or collaborate on a model without having to deal with environment configurations. 
