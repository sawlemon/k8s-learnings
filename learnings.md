# Sample snippetes

```yaml
apiVersion: v1
kind: LimitRange
metadata:
  name: limits
spec:
  limits:
  - default:
      memory: 512Mi
    defaultRequest:
      cpu: 250m
      memory: 512Mi
    type: Container
```