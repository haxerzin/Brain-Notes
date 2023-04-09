# KVM Optimization

## CPU Pinning

Add the following options to the XML file:

```xml
<iothreads>1</iothreads>
  <cputune>
  	<vcpupin vcpu="0" cpuset="2"/>
	<vcpupin vcpu="1" cpuset="3"/>
	<vcpupin vcpu="2" cpuset="4"/>
	<vcpupin vcpu="3" cpuset="5"/>
	<emulatorpin cpuset="0-1"/>
	<iothreadpin iothread="1" cpuset="0-1"/>
  </cputune>
```
