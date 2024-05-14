# webapp-by-ingress
To simplify the deployment i passed the index.html as configmap called webapp-cm

Create it by the command:

kubectl -n dev create configmap webapp-cm --from-file=website/index.html

You can use siege command to test load on the app,

Example: 

siege -c 100 -t 1M -b http://webapp.local.com