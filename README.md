# fastapi-k8s

deploy:

kubectl apply -k overlays/dev

cleanup:

kubectl delete -k overlays/dev

kubectl -n dev get secrets --no-headers=true | awk '/rethinkdb-client-pass/{print $1}'| xargs  kubectl -n dev delete secret