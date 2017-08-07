# Process to copy contents from one PVC to another

I created this to allow me to migrate from different storage backends for a given project. The process would be:

 * Create a new PVC using the preferred storage backend
 * Shutdown app (scale replicas to zero)
 * Run sync process job
 * Edit Pod specs to use new PVC
 * Scale app back up

### Usage
```
oc process -f job-template.yaml SOURCE_PVC=sourcepvc DEST_PVC=destpvc | oc create -f -
```
