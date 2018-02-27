

Finding the IPFS chart:

```
helm search ipfs
helm fetch stable/ipfs 
```

Installing a custom chart:

```
helm install transmute-ipfs


export POD_NAME=$(kubectl get pods -l "app=ipfs,release=tranmsute-ipfs"  -o jsonpath="{.items[0].metadata.name}")

kubectl port-forward $POD_NAME 5001:5001
```