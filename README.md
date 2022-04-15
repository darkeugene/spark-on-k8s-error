SparkOperator on k8s
=============================

The directory example_with_pod contains a pod that works correctly. All files located in the nfs server are visible in the container.

The directory spark_example contains SparkApplication that works incorrectly. The file contains interaction with Persistent Volume Claim according to the example given in the documentation [spark-on-k8s-operator](https://github.com/GoogleCloudPlatform/spark-on-k8s-operator/blob/master/docs/user-guide.md#mounting-volumes) but the data is from nfs server can not be viewed in the container.

The Dockerfile describes the image that is used when running sparkApplication.
The filelist.py describes the code that is executed when sparkApplication is started.


Steps to run sparkApplication:

- kubectl apply -f sc.yaml 
- kubectl apply -f pv-nfs.yaml
- kubectl apply -f pvc-nfs.yaml
- kubectl apply -f spark-py-pi.yaml **или** sparkctl create spark-py-pi.yaml
