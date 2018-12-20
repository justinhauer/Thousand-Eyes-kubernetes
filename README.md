# Thousand-Eyes-kubernetes
Thousand Eyes Enterprise Agent Deployment in kubernetes

Thousand eyes has no documentation on running their thousandeyes docker deployment in kubernetes, so I'm providing this for anyone to use. On top of this, they only provide docker run command which makes this harder to translate into a reusable container image.

#### This deployment makes a few assumptions that:
- You have a kubernetes cluster
- You have the rbac role to deploy this in your cluster in a namespace of your choice

#### There are two components:
- A secrets file with your agent token that is base64 encoded (get this from the TE dashboard when logged in)
- The deployment manifest

Run kubectl apply -f [filename] for both and you should be good. 
