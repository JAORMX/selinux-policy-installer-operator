selinux-policy-installer-operator
=================================

This is a continuation of the work that was started on:

https://github.com/JAORMX/selinux-policy-helper-operator

This operator takes the job of installing SELinux policies on your cluster. So,
the policies will be usable.

It tracks the `selinux-operator` namespace, which is the one where the
[selinux-operator](https://github.com/JAORMX/selinux-operator) is installed. It
listens for `ConfigMaps` with a certain annotation (since that's how policies
are identified on then) and it spawns privileged pods to install them on the
cluster.
