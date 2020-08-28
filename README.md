# Ticketing App

## Instructions

- Requests must be made over HTTPS

## Environment variables

```bash
# JWT_KEY
kubectl create secret generic jwt-secret --from-literal JWT_KEY=asdf

# STRIPE_KEY
kubectl create secret generic stripe-secret --from-literal STRIPE_KEY=stripe-key
```

## Expose the ingress service

```bash
# Expose the ingress service
kubectl expose deployment ingress-nginx-controller --target-port=80 --type=ClusterIP -n kube-system
```

## Dockerhub images

- Make sure all the images are hosted at DockerHub
