# Kubernetes::ExtensionsV1beta1PodSecurityPolicySpec

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_privilege_escalation** | **BOOLEAN** | allowPrivilegeEscalation determines if a pod can request to allow privilege escalation. If unspecified, defaults to true. | [optional] 
**allowed_capabilities** | **Array&lt;String&gt;** | allowedCapabilities is a list of capabilities that can be requested to add to the container. Capabilities in this field may be added at the pod author&#39;s discretion. You must not list a capability in both allowedCapabilities and requiredDropCapabilities. | [optional] 
**allowed_flex_volumes** | [**Array&lt;ExtensionsV1beta1AllowedFlexVolume&gt;**](ExtensionsV1beta1AllowedFlexVolume.md) | allowedFlexVolumes is a whitelist of allowed Flexvolumes.  Empty or nil indicates that all Flexvolumes may be used.  This parameter is effective only when the usage of the Flexvolumes is allowed in the \&quot;volumes\&quot; field. | [optional] 
**allowed_host_paths** | [**Array&lt;ExtensionsV1beta1AllowedHostPath&gt;**](ExtensionsV1beta1AllowedHostPath.md) | allowedHostPaths is a white list of allowed host paths. Empty indicates that all host paths may be used. | [optional] 
**allowed_proc_mount_types** | **Array&lt;String&gt;** | AllowedProcMountTypes is a whitelist of allowed ProcMountTypes. Empty or nil indicates that only the DefaultProcMountType may be used. This requires the ProcMountType feature flag to be enabled. | [optional] 
**allowed_unsafe_sysctls** | **Array&lt;String&gt;** | allowedUnsafeSysctls is a list of explicitly allowed unsafe sysctls, defaults to none. Each entry is either a plain sysctl name or ends in \&quot;*\&quot; in which case it is considered as a prefix of allowed sysctls. Single * means all unsafe sysctls are allowed. Kubelet has to whitelist all allowed unsafe sysctls explicitly to avoid rejection.  Examples: e.g. \&quot;foo/*\&quot; allows \&quot;foo/bar\&quot;, \&quot;foo/baz\&quot;, etc. e.g. \&quot;foo.*\&quot; allows \&quot;foo.bar\&quot;, \&quot;foo.baz\&quot;, etc. | [optional] 
**default_add_capabilities** | **Array&lt;String&gt;** | defaultAddCapabilities is the default set of capabilities that will be added to the container unless the pod spec specifically drops the capability.  You may not list a capability in both defaultAddCapabilities and requiredDropCapabilities. Capabilities added here are implicitly allowed, and need not be included in the allowedCapabilities list. | [optional] 
**default_allow_privilege_escalation** | **BOOLEAN** | defaultAllowPrivilegeEscalation controls the default setting for whether a process can gain more privileges than its parent process. | [optional] 
**forbidden_sysctls** | **Array&lt;String&gt;** | forbiddenSysctls is a list of explicitly forbidden sysctls, defaults to none. Each entry is either a plain sysctl name or ends in \&quot;*\&quot; in which case it is considered as a prefix of forbidden sysctls. Single * means all sysctls are forbidden.  Examples: e.g. \&quot;foo/*\&quot; forbids \&quot;foo/bar\&quot;, \&quot;foo/baz\&quot;, etc. e.g. \&quot;foo.*\&quot; forbids \&quot;foo.bar\&quot;, \&quot;foo.baz\&quot;, etc. | [optional] 
**fs_group** | [**ExtensionsV1beta1FSGroupStrategyOptions**](ExtensionsV1beta1FSGroupStrategyOptions.md) | fsGroup is the strategy that will dictate what fs group is used by the SecurityContext. | 
**host_ipc** | **BOOLEAN** | hostIPC determines if the policy allows the use of HostIPC in the pod spec. | [optional] 
**host_network** | **BOOLEAN** | hostNetwork determines if the policy allows the use of HostNetwork in the pod spec. | [optional] 
**host_pid** | **BOOLEAN** | hostPID determines if the policy allows the use of HostPID in the pod spec. | [optional] 
**host_ports** | [**Array&lt;ExtensionsV1beta1HostPortRange&gt;**](ExtensionsV1beta1HostPortRange.md) | hostPorts determines which host port ranges are allowed to be exposed. | [optional] 
**privileged** | **BOOLEAN** | privileged determines if a pod can request to be run as privileged. | [optional] 
**read_only_root_filesystem** | **BOOLEAN** | readOnlyRootFilesystem when set to true will force containers to run with a read only root file system.  If the container specifically requests to run with a non-read only root file system the PSP should deny the pod. If set to false the container may run with a read only root file system if it wishes but it will not be forced to. | [optional] 
**required_drop_capabilities** | **Array&lt;String&gt;** | requiredDropCapabilities are the capabilities that will be dropped from the container.  These are required to be dropped and cannot be added. | [optional] 
**run_as_group** | [**ExtensionsV1beta1RunAsGroupStrategyOptions**](ExtensionsV1beta1RunAsGroupStrategyOptions.md) | RunAsGroup is the strategy that will dictate the allowable RunAsGroup values that may be set. If this field is omitted, the pod&#39;s RunAsGroup can take any value. This field requires the RunAsGroup feature gate to be enabled. | [optional] 
**run_as_user** | [**ExtensionsV1beta1RunAsUserStrategyOptions**](ExtensionsV1beta1RunAsUserStrategyOptions.md) | runAsUser is the strategy that will dictate the allowable RunAsUser values that may be set. | 
**se_linux** | [**ExtensionsV1beta1SELinuxStrategyOptions**](ExtensionsV1beta1SELinuxStrategyOptions.md) | seLinux is the strategy that will dictate the allowable labels that may be set. | 
**supplemental_groups** | [**ExtensionsV1beta1SupplementalGroupsStrategyOptions**](ExtensionsV1beta1SupplementalGroupsStrategyOptions.md) | supplementalGroups is the strategy that will dictate what supplemental groups are used by the SecurityContext. | 
**volumes** | **Array&lt;String&gt;** | volumes is a white list of allowed volume plugins. Empty indicates that no volumes may be used. To allow all volumes you may use &#39;*&#39;. | [optional] 

