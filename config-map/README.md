# Config Map and Environment Variables

### What is a config map in Kubernetes?

- When your manifest grows it becomes difficult to manage multiple env vars
- You can take this out of the manifest and store as a config map object in the key-value pair
- Then you can inject that config map into the pod
- You can reuse the same config map into multiple pods

#### Sample command to create a config map

```bash
- kubectl create cm <configmapname> --from-literal=color=blue \
--from-literal=color=red
```
Where color=clue is the key and value of the config map