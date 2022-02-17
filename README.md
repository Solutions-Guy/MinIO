# MinIO

This MinIO setup is to run a video transcoding demo on OpenShift with 3 different Pods:

Pod 1: MinIO to manage video content (object storage on local cluster)
Pod 2: NGINX, FFMPEG and Python to pull in the video into Persistent Storage, and streaming the data out to the viewer
Pod 3: Web app with embedded video and static content, providing a solution overview 

To run the MinIO Pod, there are several steps for the OpenShift admin:

1. Deploy MinIO PVC with YML (from local machine)
2. Modify Deployment YML (change namespace, S3 access point & credentials)
3. Create Application (Right click 'D' within the topology to add app)
4. Setup the Service YML
5. Route YML (edit host, eg: host: minio-s3-mwc-vod.apps.compact2.openshift.smc) - structure: app, project name, apps, domain name)
