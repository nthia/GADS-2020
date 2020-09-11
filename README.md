# Google Africa Developer Scholarship Phase II 

## Google Cloud Practice Project

### hands-on labs on Qwiklabs provided by Pluralsight

## The challenge(s)

### The Cloud challenge parts 1:
Complete of 10-15 selected hands-on labs on Qwiklabs and submitting proof of such per screenshot based on the email received.
![ss1](https://github.com/nthia/GADS-2020/blob/master/Cloud%20Storage.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Console%20and%20Cloud%20Shell.PNG)
------------ | -------------
![ss1](https://github.com/nthia/GADS-2020/blob/master/Cloud%20IAM.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Cloud%20SQL.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Creating%20Virtual%20Machines.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Deployment%20Manager.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Error%20Reporting%20and%20Debugging.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Bastion%20Host.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Getting%20Started%20with%20Cloud%20Marketplace.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Getting%20Started%20with%20Kubernetes%20Engine.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Infrastructure%20Preview%20v1.5.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Infrastructure%20Preview%20v1.5.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Loading%20Taxi%20Data%20into%20Google%20Cloud%20SQL.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Loading%20data%20into%20BigQuery.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Resource%20Monitoring.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Running%20Apache%20Spark%20jobs%20on%20Cloud%20Dataproc.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Setting%20up%20a%20Development%20Environment%20v1.1.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Using%20BigQuery%20to%20do%20Analysis.PNG)
![ss1](https://github.com/nthia/GADS-2020/blob/master/Using%20OAuth.PNG) | ![ss1](https://github.com/nthia/GADS-2020/blob/master/Virtual%20Networking.PNG)
### The Cloud challenge parts 2:
“Translation” of 2-3 selected labs from Console instructions to 100% command line instructions.

#### Create a utility virtual machine

```console
  gcloud config set compute/zone us-central1-b && 
  gcloud compute instances create "my-vm" \
  --machine-type "n1-standard-1" \
  --image-project "debian-cloud" \
  --image "debian-9-stretch-v20190213" \
  --subnet "default"
```

#### Create a SQL Instance

```console
  gcloud sql instances create blog-db \
  --password="admin" \
  --sql-version=MYSQL_5_7" \
  --zone=us-central1-a && 
  gcloud sql databases create host-db \
  --instance="blog-db" &&
  gcloud sql users create blogdbuser \
  --instance=blog-db -i blog-db \
  --host='%' \
  --password='password'
```


