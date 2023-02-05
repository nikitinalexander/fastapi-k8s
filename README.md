# fastapi-k8s

deploy:
kubectl apply -k overlays/dev

cleanup:
kubectl delete -k overlays/dev