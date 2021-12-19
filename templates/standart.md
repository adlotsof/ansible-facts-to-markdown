# {{ ansible_hostname }}

{% for ip in ansible_facts['all_ipv4_addresses'] %}
- {{ ip }}
{% endfor %}

{% if dockerresults is defined %}
### Docker 

{% if dockerresults.containers is defined and dockerresults.containers|length > 0 %}
#### Containers running

| NAME | MOUNTS | COMMAND | PORTS | STATE |
| ---- | -----  | ------- | ----- | ----- |
{% for container in dockerresults.containers %}
| {{ container.Names }} | {% if container.Mounts|length >0 %}{% for mount in container.Mounts %} {{ mount.Name }}, {% endfor %} {% endif %} | {{ container.Command }} | {{ container.Ports }} | {{ container.State }} |
{% endfor %}

{% endif %}
{% if dockerresults.volumes is defined and dockerresults.volumes|length > 0 %}
#### Volumes
| NAME | MOUNT | DRIVER | OPTIONS | 
| ---- | -----  | ------- | ----- | 
{% for volume in dockerresults.volumes %}
| {{ volume.Name }} | {{ volume.Mountpoint }} {{ volume.Driver }} | {{ volume.Options }} | 
{% endfor %}

{% endif %}

{% if dockerresults.images is defined and dockerresults.images|length > 0 %}
#### Images
| LABELS | SIZE | 
| ---- | -----  |
{% for image in dockerresults.images %}
| {{ image.Labels }} | {{ image.Size }} {{ image.Created }} |
{% endfor %}


{% endif %}

{% endif %}

### Open Ports

#### TCP

| name | user | port | adress |
| --- | --- | --- | --- |
{% for port in ansible_facts['tcp_listen'] %}
| {{ port.name }} | {{ port.user }} | {{ port.port }} | {{ port.address }} |
{% endfor %}


#### UDP

| name | user | port | adress |
| --- | --- | --- | --- |
{% for port in ansible_facts['udp_listen'] %}
| {{ port.name }} | {{ port.user }} | {{ port.port }} | {{ port.address }} |
{% endfor %}
| --- | --- | --- | --- | --- |

## Hardware

### Memory

| - | total | free | used |
| ----- | --- | --- | --- | 
| Memory| {{ ansible_facts['memory_mb'].real.total }} | {{ ansible_facts['memory_mb'].real.free }} | {{ ansible_facts['memory_mb'].real.used }} |
| Swap | {{ ansible_facts['memory_mb'].swap.total }}  | {{ ansible_facts['memory_mb'].swap.free }} | {{ ansible_facts['memory_mb'].swap.used }} |
| total | {{ ansible_facts['memtotal_mb'] }} |  |  | 
### CPUs


| Type| Count | Cores | Vcpus |
| --- | --- | --- | --- |
| {{ ansible_facts['processor'][2] }} | {{ ansible_facts['processor_count'] }} | {{ ansible_facts['processor_cores'] }} | {{ ansible_facts['processor_vcpus'] }} |


### Mounts


| device | type | mount | total | available |
| --- | --- | --- | --- | --- |
{% for mount in ansible_facts['mounts'] %}
| {{mount.device }} | {{ mount.fstype }} | {{ mount.mount }} | {{ mount.size_total }}| {{ mount.size_available }} |
{% endfor %}


### Interfaces

{% for interface in ansible_facts['interfaces'] %}
- {{interface}}
{% endfor %}



## Software

{% if ansible_facts['lsb'] is defined %}
### OS
|  -  |  -  |
| --- | --- |
| id | {{ ansible_facts['lsb'].id }} |
| description | {{ ansible_facts['lsb'].description }} {{ ansible_facts['lsb'].codename }} |
| release | {{ ansible_facts['lsb'].release }} |
| kernel | {{ ansible_facts['kernel'] }} |
{% endif %}
### Upgradable apt

--------
{% for line in upgradable %}
{{ line }}
{% endfor %}
--------

ansible localhost -b -K -a "apt list --upgradable"

### Git Status

{% for path in git_paths %}
#### {{ path.path }}
{% for line in  path.status %}
{{line}}
{% endfor %}
{% endfor %}



