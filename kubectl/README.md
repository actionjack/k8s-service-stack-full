# kubectl brain dump

You need to run this command a few times to complete the initial deploy. Don't let this get you down, Kubernetes is a convergent system and ordering is too loose to rely on. That's a good thing, it's by design and yields a far more resilient architecture, so feel good each time you run the command and see less errors.
```
# Run until config has converged
kubectl apply --recursive -f .
```

