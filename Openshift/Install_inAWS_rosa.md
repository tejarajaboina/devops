# How to deploy Openshift cluster in AWS
we have a fabulos tool called rosa to help us in deploying openshift on AWS

## Prerequisets
* Install AWS CLI
* Install rosa 
    - download from [here](https://console.redhat.com/openshift/downloads#tool-rosa)
## Configure/connect
* AWS
```
aws configure
```
* ROSA
```
login rosa
```
- for login token check [this](https://console.redhat.com/openshift/token/rosa)
# log into rosa get password from openshift redhat 
rosa login 

#check few this as below
rosa verify permissions
rosa verify quota
rosa init

# Create using single command
rosa create cluster \
      --cluster-name=istio-test-1 \
      --version=4.7.28 \
      --compute-machine-type=m5.xlarge \
      --compute-nodes=2 \
      --machine-cidr=10.1.0.0/24 \
      --region=ap-south-1
	  
# Create using interactive command
rosa create cluster --interactive

#Create admin user 

rosa create admin --cluster istio-test-1

#
oc login https://api.istio-test-1.e2qt.p1.openshiftapps.com:6443 --username cluster-admin --password ZnUof-BDGrW-9VK9d-f5rZ4
cluster-admin --password ZnUof-BDGrW-9VK9d-f5rZ4


#How to delete cluster 
rosa delete cluster --cluster istio-test-1

#delete Stack
rosa init --delete-stack
