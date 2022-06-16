
## LM Container title
 


## Argus Helm Chart Configuration Schema
 The Argus Helm Chart Configuration Schema

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.clusterName | Friendly Cluster Name | The unique name to give to the cluster's resource group.<br>NOTE: You must not change the name once the application is deployed in the cluster. If changed, breaks correlation at multiple places<br>example: Organised Resource group name of Kubernetes resource tree, is generated as "Kubernetes Cluster: <clusterName>" |
| .argus.affinity | affinity | Affinity allows you to constrain which nodes your pod is eligible to be scheduled on. |
| .argus.labels | The Argus extra labels schema | Labels to apply on all objects created by Argus. Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels |
| .argus.ignoreSSL | The ignoreSSL Schema | Set flag to ignore ssl/tls validation. |
| .argus.accessID | Logicmonitor API Token accessID | The LogicMonitor API key ID.<br>NOTE: Ensure to add surrounding double quotes to avoid special character parsing errors. |
| .argus.priorityClassName | priorityClassName | The priority class name for Pod priority. If the priorityClassName parameter is enabled, then PriorityClass resource is created, or the Pod is rejected. |
| .argus.resourceContainerID | The resourceContainerID schema | You must use the resourceContainerID when you install Argus as a non-admin user. <br>The resourceContainerID is a parent resource group id that holds all cluster resources under it. |
| .argus.enabled |  | Defined for umbrella chart but unused here. |
| .argus.clusterTreeParentID | The clusterTreeParentID | clusterTreeParentID is a parent static resource group ID under which the organised Kubernetes resource tree gets created.<br>A static resource group with the mentioned ID should exit beforehand. |
| .argus.nodeSelector | nodeSelector | NodeSelector is a selector, which must be set to true for the pod to fit on a node. The selector must match the node's labels for the pod to be scheduled on that node. More info: https://kubernetes.io/docs/concepts/configuration/assign-pod-node/ |
| .argus.etcdDiscoveryToken | The ETCD DiscoveryToken Schema | The ETCD DiscoveryToken. |
| .argus.replicas | The replicas schema | Argus Pod Replicas - defaults to 1, parameter is just for development purpose, do not increase more than one replicas in production |
| .argus.kube-state-metrics |  |  |
| .argus.nameOverride | The nameOverride schema | Describes the purpose of this instance. |
| .argus.accessKey | Logicmonitor API Token accessKey | The LogicMonitor API key.<br>NOTE: Ensure to add surrounding double quotes to avoid special character parsing errors. |
| .argus.account | Logicmonitor account name | The LogicMonitor account name.nValue should be trimmed from URL "___.logicmonitor.com"<br>example: lmqauat.logicmonitor.com then "lmqauat" must be a valid value. |
| .argus.annotations | The Argus extra annotations schema | Annotations to apply on all objects created by Argus. Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations |
| .argus.fullnameOverride | The fullnameOverride schema | Describes the purpose of this instance. |

## The debug schema
 The Application debugging configurations.


## The profiling schema
 Profile generation configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.debug.profiling.enable | The enable schema | Once the property is set to true, it starts application profile generations. |

## The serviceAccount schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.serviceAccount.create | The create schema | Describes the purpose of this instance. |

## tolerations
 tolerations are applied to pods, and allow the pods to schedule onto nodes with matching taints.


## .argus.tolerations[*] title
 


## .argus.tolerations[*].optionalSchema[0] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.tolerations[*].optionalSchema[0].value |  | Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string. |
| .argus.tolerations[*].optionalSchema[0].effect |  | Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute. |
| .argus.tolerations[*].optionalSchema[0].key |  | Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys. |
| .argus.tolerations[*].optionalSchema[0].operator |  | Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category. |
| .argus.tolerations[*].optionalSchema[0].tolerationSeconds |  | TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system. |

## .argus.tolerations[*].optionalSchema[1] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.tolerations[*].optionalSchema[1].effect |  | Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute. |
| .argus.tolerations[*].optionalSchema[1].key |  | Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys. |
| .argus.tolerations[*].optionalSchema[1].operator |  | Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category. |
| .argus.tolerations[*].optionalSchema[1].tolerationSeconds |  | TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system. |
| .argus.tolerations[*].optionalSchema[1].value |  | Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string. |

## Argus Docker Image Schema
 The image contains the Argus docker image details.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.image.registry | Argus Image Registry Schema | The Docker Registry from which Argus image is pulled.<br>defaults to empty value. |
| .argus.image.repository | Argus Image Repository Schema | The Docker Repository Name for Argus Image |
| .argus.image.pullPolicy | The Argus pullPolicy Schema | Overrides the image pullPolicy.<br>Defaults to "Always". |
| .argus.image.tag | The Argus Image tag schema | The Argus Docker Image Tag.<br>Overrides the image tag whose default is the chart appVersion. |

## The proxy schema
 The Http/s proxy for Argus

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.proxy.user | The Proxy Server's User schema | User for the Proxy Server. |
| .argus.proxy.pass | The Proxy Server's Password schema | Password for the Proxy Server |
| .argus.proxy.url | The Proxy Server URL Schema | The Proxy Server's URL |

## The collector schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.version | The version schema | Describes the purpose of this instance. |
| .argus.collector.size | The size schema | Describes the purpose of this instance. |
| .argus.collector.annotations | The annotations schema | Describes the purpose of this instance. |
| .argus.collector.replicas | The replicas schema | Describes the purpose of this instance. |
| .argus.collector.useEA | The useEA schema | Describes the purpose of this instance. |
| .argus.collector.labels | The labels schema | Describes the purpose of this instance. |

## .argus.collector.probe title
 The container probe configuration schema.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.probe.enabled |  | Enables container probes. |

## .argus.collector.probe.startup title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.probe.startup.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the Argus startup. |
| .argus.collector.probe.startup.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .argus.collector.probe.liveness title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.probe.liveness.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the argus startup |
| .argus.collector.probe.liveness.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .argus.collector.probe.readiness title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.probe.readiness.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the Argus startup |
| .argus.collector.probe.readiness.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## The image schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.image.registry | The registry schema | Container Image Registry |
| .argus.collector.image.repository | The repository schema | Describes the purpose of this instance. |
| .argus.collector.image.tag | The tag schema | Describes the purpose of this instance. |
| .argus.collector.image.pullPolicy | The pullPolicy schema | Describes the purpose of this instance. |

## .argus.collector.statefulsetSpec title
 The collector StatefulSet specification for customizations


## .argus.collector.statefulsetSpec.template title
 


## .argus.collector.statefulsetSpec.template.spec title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.priorityClassName |  | If specified, indicates the pod's priority. "system-node-critical" and "system-cluster-critical" are two special keywords that indicate the highest priorities with the former being the highest priority. Any other name must be defined while creating a PriorityClass object with that name. If not specified, the pod priority will be default or zero if there is no default. |
| .argus.collector.statefulsetSpec.template.spec.schedulerName |  | If specified, the pod will be dispatched by specified scheduler. If not specified, the pod will be dispatched by default scheduler. |
| .argus.collector.statefulsetSpec.template.spec.nodeSelector |  | NodeSelector is a selector, which you must set to true for the pod to fit on a node. The selector must match a node's labels for the pod to be scheduled on that node. More info: https://kubernetes.io/docs/concepts/configuration/assign-pod-node/ |
| .argus.collector.statefulsetSpec.template.spec.priority |  | The priority value. Various system components use the property value field to find the priority of the pod. When Priority Admission Controller is enabled, it prevents users from setting this field. The Admission Controller populates this field from PriorityClassName. The higher the value, the higher the priority. |
| .argus.collector.statefulsetSpec.template.spec.nodeName |  | NodeName is a request to schedule this pod onto a specific node. If it is non-empty, the scheduler simply schedules this pod onto that node, assuming that it fits resource requirements. |
| .argus.collector.statefulsetSpec.template.spec.restartPolicy |  | Restart policy for all containers within the pod. One of Always, OnFailure, Never. Set the default value to Always. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy |
| .argus.collector.statefulsetSpec.template.spec.dnsPolicy |  | Set DNS policy for the pod. Defaults to "ClusterFirst". Valid values are 'ClusterFirstWithHostNet', 'ClusterFirst', 'Default' or 'None'. DNS parameters given in DNSConfig will be merged with the policy selected with DNSPolicy. To have DNS options set along with hostNetwork, you have to specify DNS policy explicitly to 'ClusterFirstWithHostNet'. |

## .argus.collector.statefulsetSpec.template.spec.tolerations title
 


## .argus.collector.statefulsetSpec.template.spec.tolerations[*] title
 


## .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[0] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[0].value |  | Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[0].effect |  | Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[0].key |  | Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[0].operator |  | Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[0].tolerationSeconds |  | TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system. |

## .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[1] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[1].effect |  | Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[1].key |  | Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[1].operator |  | Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[1].tolerationSeconds |  | TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system. |
| .argus.collector.statefulsetSpec.template.spec.tolerations[*].optionalSchema[1].value |  | Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string. |

## .argus.collector.statefulsetSpec.template.spec.dnsConfig title
 PodDNSConfig defines the DNS parameters of a pod in addition to those generated from DNSPolicy.


## .argus.collector.statefulsetSpec.template.spec.dnsConfig.nameservers title
 A list of DNS name server IP addresses. This will be appended to the base nameservers generated from DNSPolicy. Duplicated nameservers will be removed.


## .argus.collector.statefulsetSpec.template.spec.dnsConfig.nameservers[*] title
 


## .argus.collector.statefulsetSpec.template.spec.dnsConfig.options title
 A list of DNS resolver options. This will be merged with the base options generated from DNSPolicy. Duplicated entries will be removed. Resolution options given in Options will override those that appear in the base DNSPolicy.


## .argus.collector.statefulsetSpec.template.spec.dnsConfig.options[*] title
 PodDNSConfigOption defines DNS resolver options of a pod.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.dnsConfig.options[*].name |  | Required. |
| .argus.collector.statefulsetSpec.template.spec.dnsConfig.options[*].value |  |  |

## .argus.collector.statefulsetSpec.template.spec.dnsConfig.searches title
 A list of DNS search domains for host-name lookup. This will be appended to the base search paths generated from DNSPolicy. Duplicated search paths will be removed.


## .argus.collector.statefulsetSpec.template.spec.dnsConfig.searches[*] title
 


## .argus.collector.statefulsetSpec.template.spec.volumes title
 List of volumes that can be mounted by containers belonging to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes


## .argus.collector.statefulsetSpec.template.spec.volumes[*] title
 Volume represents a named volume in a pod that may be accessed by any container in the pod.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].name |  | Volume's name. Must be a DNS_LABEL and unique within the pod. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk title
 AzureDisk represents an Azure Data Disk mount on the host and bind mount to the pod.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk.cachingMode |  | Host Caching mode: None, Read Only, Read Write. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk.diskName |  | The name of the data disk in the blob storage. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk.diskURI |  | The URI of the data disk in the blob storage |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk.fsType |  | Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk.kind |  | Expected values Shared: multiple blob disks per storage account  Dedicated: single blob disk per storage account  Managed: Azure managed data disk (only in managed availability set). defaults to shared |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].azureDisk.readOnly |  | By default, the propertu is set to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts. |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap title
 Adapts a ConfigMap into a volume.

The contents of the target ConfigMap's Data field will be presented in a volume as files using the keys in the Data field as the file names, unless the items element is populated with specific mappings of keys to paths. ConfigMap volumes support ownership management and SELinux relabeling.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.defaultMode |  | Optional: mode bits to use on created files by default. Must be a value between 0 and 0777. Defaults to 0644. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.name |  | Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.optional |  | Specify whether the ConfigMap or it's keys must be defined |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.items title
 If not specified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified and is not present in the ConfigMap, the volume setup will display an error unless it is marked optional. Paths must be relative and must not contain the '..' path or start with '..'.


## .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.items[*] title
 Maps a string key to a path within a volume.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.items[*].path |  | The relative path of the file to map the key to. This may not be an absolute path. May not contain the path element '..'. May not start with the string '..'. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.items[*].key |  | The key to project. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].configMap.items[*].mode |  | Optional, mode bits to use on this file, must be a value between 0 and 0777. If not specified, the defalut volume for mode will be used. This could create conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set. |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].emptyDir title
 Represents an empty directory for a pod. Empty directory volumes support ownership management and SELinux relabeling.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].emptyDir.medium |  | Specifies the type of storage medium should back this directory. The default is "" which means to use the node's default medium. Must be an empty string (default) or Memory. More info: https://kubernetes.io/docs/concepts/storage/volumes#emptydir |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].emptyDir.sizeLimit |  | Total amount of local storage required for this EmptyDir volume. The size limit is also applicable for memory medium. The maximum usage on memory medium EmptyDir would be the minimum value between the SizeLimit specified here and the sum of memory limits of all containers in a pod. The default is nil which means that the limit is undefined. More info: https://kubernetes.io/docs/user-guide/volumes#emptydir |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].hostPath title
 Represents a host path mapped into a pod. Host path volumes do not support ownership management or SELinux relabeling.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].hostPath.path |  | Path of the directory on the host. If the path is a symlink, it will follow the link to the real path. More info: https://kubernetes.io/docs/concepts/storage/volumes#hostpath |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].hostPath.type |  | Type for HostPath Volume, by default is set to "" More info: https://kubernetes.io/docs/concepts/storage/volumes#hostpath |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].persistentVolumeClaim title
 PersistentVolumeClaimVolumeSource references the user's PVC in the same namespace. This volume finds the bound PV and mounts that volume for the pod. A PersistentVolumeClaimVolumeSource is, essentially, a wrapper around another type of volume that is owned by someone else (the system).

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].persistentVolumeClaim.readOnly |  | Will force the ReadOnly setting in VolumeMounts. Default false. |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].persistentVolumeClaim.claimName |  | ClaimName is the name of a PersistentVolumeClaim in the same namespace as the pod using this volume. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims |

## .argus.collector.statefulsetSpec.template.spec.volumes[*].awsElasticBlockStore title
 Represents a Persistent Disk resource in AWS.

You must exit the AWS EBS disk before mounting to a container. The disk must also be in the same AWS zone as the kubelet. An AWS EBS disk can only be mounted as read/write once. AWS EBS volumes support ownership management and SELinux relabeling.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].awsElasticBlockStore.fsType |  | Filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].awsElasticBlockStore.partition |  | The partition in the volume that you want to mount. If omitted, by default it mounts by volume name. Examples: For volume /dev/sda1, you specify the partition as "1". Similarly, the volume partition for /dev/sda is "0" (or you can leave the property empty). |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].awsElasticBlockStore.readOnly |  | Specify "true" to force and set the ReadOnly property in VolumeMounts to "true". If omitted, the default is set to "false". More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore |
| .argus.collector.statefulsetSpec.template.spec.volumes[*].awsElasticBlockStore.volumeID |  | Unique ID of the persistent disk resource in AWS (Amazon EBS volume). More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore |

## .argus.collector.statefulsetSpec.template.spec.containers title
 


## .argus.collector.statefulsetSpec.template.spec.containers[*] title
 A single application container that you want to run within a pod.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.containers[*].name |  |  |

## .argus.collector.statefulsetSpec.template.spec.containers[*].resources title
 Compute Resources required by this container. Cannot be updated. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.containers[*].resources.limits |  | Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/ |
| .argus.collector.statefulsetSpec.template.spec.containers[*].resources.requests |  | Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/ |

## .argus.collector.statefulsetSpec.template.spec.hostAliases title
 HostAliases is an optional list of hosts and IPs that will be injected into the pod's hosts file if specified. This is only valid for non-hostNetwork pods.


## .argus.collector.statefulsetSpec.template.spec.hostAliases[*] title
 HostAlias holds the mapping between IP and hostnames that will be injected as an entry in the pod's hosts file.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.statefulsetSpec.template.spec.hostAliases[*].ip |  | IP address of the host file entry. |

## .argus.collector.statefulsetSpec.template.spec.hostAliases[*].hostnames title
 Hostnames for the above IP address.


## .argus.collector.statefulsetSpec.template.spec.hostAliases[*].hostnames[*] title
 


## The lm schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.lm.groupID | The groupID schema | Describes the purpose of this instance. |
| .argus.collector.lm.escalationChainID | The escalationChainID schema | Describes the purpose of this instance. |

## The proxy schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collector.proxy.url | The url schema | Describes the purpose of this instance. |
| .argus.collector.proxy.user | The user schema | Describes the purpose of this instance. |
| .argus.collector.proxy.pass | The pass schema | Describes the purpose of this instance. |

## The rbac schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.rbac.create | The create schema | Describes the purpose of this instance. |

## The collectorsetcontroller schema
 The Collectorset-Controller Configurations

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.collectorsetcontroller.address | The CollectorsetController Address Schema | The Collectorset-controller grpc service address |
| .argus.collectorsetcontroller.port | port | The Collectorset-controller grpc service port |

## The filters schema
 Set of filter rules to exclude from adding into LogicMonitor.


## .argus.filters[*] title
 


## The Argus resource limits schema
 The Argus pod resource limits

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.resources.limits |  | Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/ |
| .argus.resources.requests |  | Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/ |

## The Logicmonitor Portal Configurations
 The settings or configurations which reflect on LogicMonitor portal.


## The LMLogs schema
 The LogicMonitor Logs collection settings.


## The Kubernetes Events schema
 The Kubernetes Events collection configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.lm.lmlogs.k8sevent.enable | The enable schema | Once you enable the property, it starts collecting Kuberentes events. |

## The k8spodlog schema.
 Kubernetes Pod Logs collection configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.lm.lmlogs.k8spodlog.enable | The enable schema | Once you enable the property, it starts Kuberentes Pod's logs collection |

## The resource schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.lm.resource.globalDeleteAfterDuration | The globalDeleteAfterDuration schema | Global scheduled delete duration to delete resources after, values must be in ISO8601 format |

## The alerting schema
 Alerting settings to apply to resource groups.
Only cluster scoped resources are valid here.
 If any Namespace scoped resources are set, then the namespance resources will get ignored.


## The disable schema
 Set of resources to set disable upon resource groups.
Only cluster scoped resources are valid here.
If any Namespace scoped resources are set, then the namespance resources will get ignored.


## .argus.lm.resource.alerting.disable[*] title
 


## The resourceGroup schema
 Resource Group Settings


## The extraProps schema
 Extra properties to add upon resource groups, only cluster scoped resources are valid, for others resources use namespace labels


## The cluster schema
 Properties to apply upon cluster tree root resource group.


## .argus.lm.resourceGroup.extraProps.cluster[*] title
 


## .argus.lm.resourceGroup.extraProps.cluster[*] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.lm.resourceGroup.extraProps.cluster[*].name |  |  |
| .argus.lm.resourceGroup.extraProps.cluster[*].value |  |  |
| .argus.lm.resourceGroup.extraProps.cluster[*].override |  |  |

## Properties to apply upon Nodes resource group.
 


## .argus.lm.resourceGroup.extraProps.nodes[*] title
 


## .argus.lm.resourceGroup.extraProps.nodes[*] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.lm.resourceGroup.extraProps.nodes[*].name |  |  |
| .argus.lm.resourceGroup.extraProps.nodes[*].value |  |  |
| .argus.lm.resourceGroup.extraProps.nodes[*].override |  |  |

## The etcd schema
 Properties to apply upon ETCD resource group.


## .argus.lm.resourceGroup.extraProps.etcd[*] title
 


## .argus.lm.resourceGroup.extraProps.etcd[*] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.lm.resourceGroup.extraProps.etcd[*].name |  |  |
| .argus.lm.resourceGroup.extraProps.etcd[*].value |  |  |
| .argus.lm.resourceGroup.extraProps.etcd[*].override |  |  |

## .argus.probe title
 The container probe configuration schema

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.probe.enabled |  | Enables container probes. |

## .argus.probe.startup title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.probe.startup.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the Argus startup. |
| .argus.probe.startup.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .argus.probe.liveness title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.probe.liveness.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the Argus startup |
| .argus.probe.liveness.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .argus.probe.readiness title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.probe.readiness.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the Argus startup |
| .argus.probe.readiness.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .argus.imagePullSecrets title
 ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. For example, in the case of docker, only DockerConfig type secrets are honored. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod


## .argus.imagePullSecrets[*] title
 


## .argus.imagePullSecrets[*] title
 LocalObjectReference contains information to locate the referenced object inside the same namespace.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.imagePullSecrets[*].name |  | Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |

## .argus.global title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.global.collectorsetServiceNameSuffix |  | Suffix to be added to .Release.name to generate Collectorset controller service URL.<br>Keep it empty while installing this chart individually, umbrella chart uses this to generate unique name across. |
| .argus.global.accessID | Logicmonitor API Token accessID | The LogicMonitor API key ID.<br>NOTE: Ensure to add surrounding double quotes to avoid special character parsing errors. |
| .argus.global.accessKey | Logicmonitor API Token accessKey | The LogicMonitor API key.<br>NOTE: Ensure to add surrounding double quotes to avoid special character parsing errors. |
| .argus.global.account | Logicmonitor account name | The LogicMonitor account name.nValue should be trimmed from URL "___.logicmonitor.com"<br>example: lmqauat.logicmonitor.com then "lmqauat" must be a valid value. |

## .argus.global.imagePullSecrets title
 ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. For example, in the case of docker, only DockerConfig type secrets are honored. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod


## .argus.global.imagePullSecrets[*] title
 


## .argus.global.imagePullSecrets[*] title
 LocalObjectReference contains information to locate the referenced object inside the same namespace.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.global.imagePullSecrets[*].name |  | Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |

## The image schema
 Describes the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.global.image.registry | The registry schema | Container Image Registry. |
| .argus.global.image.pullPolicy | pullPolicy | Overrides the image tag whose default is the chart appVersion. |

## proxy
 Http/s proxy

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.global.proxy.url | url | Proxy service endpoint. |
| .argus.global.proxy.user | The user schema | User for Proxy service. |
| .argus.global.proxy.pass | pass | Password for the Proxy service. |

## The selfMonitor schema
 Configurations to expose self monitor metrics in Openmetrics format.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.selfMonitor.enable | The enable schema | Once the property is enabled, self monitor metrics are displayed.  |
| .argus.selfMonitor.port | The port schema | port number to expose self monitor "/metrics" endpoint |

## Log
 The Argus Log Configurations Schema

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.log.level | The Log Level for Argus Schema | The Log Level for Argus |

## The Argus Daemon configurations Schema
 The Argus Daemon configurations.


## The Kubernetes watcher configurations Schema
 The Kubernetes watcher configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.daemons.watcher.bulkSyncInterval | bulkSyncInterval | The Bulk Discovery Run Interval Duration. |
| .argus.daemons.watcher.sysIpsWaitTimeout | The sysIpsWaitTimeout schema | The sysIpsWaitTimeout is a timout for argus to wait till Logicmonitor portal copies system.hostname value into system.ips for updated IP of resource |

## The runner configurations schema
 The configurations for parallel runners to process watcher events.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.daemons.watcher.runner.poolSize | The Runner poolSize schema | The number runners in a pool. |
| .argus.daemons.watcher.runner.backPressureQueueSizePerRunner | The Number of events to queue per runner schema | The number of events to queue per runner. |

## The LM Resource sweeper configurations Schema
 The LM Resource sweeper configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.daemons.lmResourceSweeper.interval | The LogicMonitor Resource sweeper Interval Schema | The LogicMonitor Resource sweeper Run Interval Duration. |

## The Cache Sync using LogicMonitor resources configurations Schema
 The Cache Sync using LogicMonitor resources configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.daemons.lmCacheSync.interval | The Cache Sync using LogicMonitor resources Interval Schema | The Cache Sync using LogicMonitor resources Run Interval Duration. |

## The Worker configurations Schema
 The Worker configurations.

| Path | Title | Description |
| :---- | :---- | :---- |
| .argus.daemons.worker.poolSize | The Worker poolSize schema | The number of workers in a pool. |

## The monitoring schema
 The Monitoring settings


## The disable schema
 Set of resource names to disable monitoring for.


## .argus.monitoring.disable[*] title
 


## Collectorset Controller Helm chart Values Schema
 Collectorset Controller Helm chart Values Schema

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.nameOverride | The nameOverride schema | An explanation about the purpose of this instance. |
| .collectorset-controller.affinity | The affinity schema | An explanation about the purpose of this instance. |
| .collectorset-controller.priorityClassName | The priorityClassName schema | An explanation about the purpose of this instance. |
| .collectorset-controller.enabled |  | Defined for umbrella chart but unused here. |
| .collectorset-controller.nodeSelector | The nodeSelector schema | NodeSelector is a selector which must be true for the pod to fit on a node. Selector which must match a node's labels for the pod to be scheduled on that node. More info: https://kubernetes.io/docs/concepts/configuration/assign-pod-node/ |
| .collectorset-controller.accessID | The accessID schema | An explanation about the purpose of this instance. |
| .collectorset-controller.labels | The labels schema | An explanation about the purpose of this instance. |
| .collectorset-controller.annotations | The annotations schema | An explanation about the purpose of this instance. |
| .collectorset-controller.fullnameOverride | The fullnameOverride schema | An explanation about the purpose of this instance. |
| .collectorset-controller.account | The account schema | An explanation about the purpose of this instance. |
| .collectorset-controller.ignoreSSL | The ignoreSSL schema | An explanation about the purpose of this instance. |
| .collectorset-controller.accessKey | The accessKey schema | An explanation about the purpose of this instance. |

## The log schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.log.level | The level schema | An explanation about the purpose of this instance. |

## The rbac schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.rbac.create | The create schema | An explanation about the purpose of this instance. |

## The proxy schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.proxy.url | The url schema | An explanation about the purpose of this instance. |
| .collectorset-controller.proxy.user | The user schema | An explanation about the purpose of this instance. |
| .collectorset-controller.proxy.pass | The pass schema | An explanation about the purpose of this instance. |

## .collectorset-controller.imagePullSecrets title
 ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. For example, in the case of docker, only DockerConfig type secrets are honored. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod


## .collectorset-controller.imagePullSecrets[*] title
 


## .collectorset-controller.imagePullSecrets[*] title
 LocalObjectReference contains enough information to let you locate the referenced object inside the same namespace.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.imagePullSecrets[*].name |  | Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |

## The serviceAccount schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.serviceAccount.create | The create schema | An explanation about the purpose of this instance. |

## The image schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.image.registry | The registry schema | Container Image Registry |
| .collectorset-controller.image.repository | The repository schema | An explanation about the purpose of this instance. |
| .collectorset-controller.image.pullPolicy | The pullPolicy schema | An explanation about the purpose of this instance. |
| .collectorset-controller.image.tag | The tag schema | An explanation about the purpose of this instance. |

## The tolerations schema
 An explanation about the purpose of this instance.


## .collectorset-controller.tolerations[*] title
 


## .collectorset-controller.tolerations[*].optionalSchema[0] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.tolerations[*].optionalSchema[0].value |  | Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string. |
| .collectorset-controller.tolerations[*].optionalSchema[0].effect |  | Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute. |
| .collectorset-controller.tolerations[*].optionalSchema[0].key |  | Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys. |
| .collectorset-controller.tolerations[*].optionalSchema[0].operator |  | Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category. |
| .collectorset-controller.tolerations[*].optionalSchema[0].tolerationSeconds |  | TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system. |

## .collectorset-controller.tolerations[*].optionalSchema[1] title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.tolerations[*].optionalSchema[1].value |  | Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string. |
| .collectorset-controller.tolerations[*].optionalSchema[1].effect |  | Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute. |
| .collectorset-controller.tolerations[*].optionalSchema[1].key |  | Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys. |
| .collectorset-controller.tolerations[*].optionalSchema[1].operator |  | Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category. |
| .collectorset-controller.tolerations[*].optionalSchema[1].tolerationSeconds |  | TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system. |

## .collectorset-controller.global title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.global.collectorsetServiceNameSuffix |  | Suffix to be added to .Release.name to generate Collectorset controller service name.<br>Keep it empty while installing this chart individually, umbrella chart uses this to generate unique name across |

## .collectorset-controller.global.imagePullSecrets title
 ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. For example, in the case of docker, only DockerConfig type secrets are honored. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod


## .collectorset-controller.global.imagePullSecrets[*] title
 


## .collectorset-controller.global.imagePullSecrets[*] title
 LocalObjectReference contains enough information to let you locate the referenced object inside the same namespace.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.global.imagePullSecrets[*].name |  | Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names |

## The image schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.global.image.registry | The registry schema | Container Image Registry |
| .collectorset-controller.global.image.pullPolicy | pullPolicy | Overrides the image tag whose default is the chart appVersion. |

## The proxy schema
 An explanation about the purpose of this instance.

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.global.proxy.pass | The pass schema | An explanation about the purpose of this instance. |
| .collectorset-controller.global.proxy.url | The url schema | An explanation about the purpose of this instance. |
| .collectorset-controller.global.proxy.user | The user schema | An explanation about the purpose of this instance. |

## .collectorset-controller.probe title
 The container probe configuration schema

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.probe.enabled |  | Enables container probes |

## .collectorset-controller.probe.startup title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.probe.startup.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the argus startup |
| .collectorset-controller.probe.startup.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .collectorset-controller.probe.liveness title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.probe.liveness.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the argus startup |
| .collectorset-controller.probe.liveness.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |

## .collectorset-controller.probe.readiness title
 

| Path | Title | Description |
| :---- | :---- | :---- |
| .collectorset-controller.probe.readiness.failureThreshold |  | The failureThreshold is maximum count before marking container start failed, typically collector installation time affects the argus startup |
| .collectorset-controller.probe.readiness.periodSeconds |  | How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. |
{}
