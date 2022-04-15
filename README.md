SparkOperator on k8s
=============================

The directory example_with_pod contains a pod that works correctly. All files located in the nfs server are visible in the container.

The directory spark_example contains SparkApplication that works incorrectly. The file contains interaction with Persistent Volume Claim according to the example given in the documentation [spark-on-k8s-operator](https://github.com/GoogleCloudPlatform/spark-on-k8s-operator/blob/master/docs/user-guide.md#mounting-volumes) but the data is from nfs server can not be viewed in the container.
