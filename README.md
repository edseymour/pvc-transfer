# Process to copy contents from one PVC to another

### Usage
```
oc process -f job-template.yaml SOURCE_PVC=sourcepvc DEST_PVC=destpvc | oc create -f -
```
