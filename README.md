[![Build Status](https://travis-ci.org/microdc/k8s-service-stack-full.svg?branch=master)](https://travis-ci.org/microdc/k8s-service-stack-full)

# k8s-service-stack-full
temp repo to house the full service configuration while we split it


# Notes for running on bare metal
- Remove kube2iam from kube-system namespace
- change elasticsearch-data-statefulset.yaml to use emptyDir instead of a persistentVolumeClaim:
```
      volumes:
        - name: startup
          configMap:
            name: elasticsearch-startup-1
        - name: elasticsearch-data
          emptyDir: {}
```
- Ensure sysctl settings are set on the nodes:
  vm.max_map_count=262144
