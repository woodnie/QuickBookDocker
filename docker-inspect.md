\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES

06fb54229654        centos              "/bin/bash -c 'whileΓÇª"   5 minutes ago       Up 5 minutes                            dazzling\_vaughan



\[root@localhost ~\]\# docker inspect 06fb54229654

\[

    {

        "Id": "06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f",

        "Created": "2020-01-21T14:58:46.323049537Z",

        "Path": "/bin/bash",

        "Args": \[

            "-c",

            "while true; do echo hello world; sleep 2;done"

        \],

        "State": {

            "Status": "running",

            "Running": true,

            "Paused": false,

            "Restarting": false,

            "OOMKilled": false,

            "Dead": false,

            "Pid": 27831,

            "ExitCode": 0,

            "Error": "",

            "StartedAt": "2020-01-21T14:58:46.566305691Z",

            "FinishedAt": "0001-01-01T00:00:00Z"

        },

        "Image": "sha256:470671670cac686c7cf0081e0b37da2e9f4f768ddc5f6a26102ccd1c6954c1ee",

        "ResolvConfPath": "/var/lib/docker/containers/06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f/resolv.conf",

        "HostnamePath": "/var/lib/docker/containers/06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f/hostname",

        "HostsPath": "/var/lib/docker/containers/06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f/hosts",

        "LogPath": "/var/lib/docker/containers/06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f/06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f-json.log",

        "Name": "/dazzling\_vaughan",

        "RestartCount": 0,

        "Driver": "overlay2",

        "Platform": "linux",

        "MountLabel": "",

        "ProcessLabel": "",

        "AppArmorProfile": "",

        "ExecIDs": null,

        "HostConfig": {

            "Binds": null,

            "ContainerIDFile": "",

            "LogConfig": {

                "Type": "json-file",

                "Config": {}

            },

            "NetworkMode": "default",

            "PortBindings": {},

            "RestartPolicy": {

                "Name": "no",

                "MaximumRetryCount": 0

            },

            "AutoRemove": false,

            "VolumeDriver": "",

            "VolumesFrom": null,

            "CapAdd": null,

            "CapDrop": null,

            "Capabilities": null,

            "Dns": \[\],

            "DnsOptions": \[\],

            "DnsSearch": \[\],

            "ExtraHosts": null,

            "GroupAdd": null,

            "IpcMode": "private",

            "Cgroup": "",

            "Links": null,

            "OomScoreAdj": 0,

            "PidMode": "",

            "Privileged": false,

            "PublishAllPorts": false,

            "ReadonlyRootfs": false,

            "SecurityOpt": null,

            "UTSMode": "",

            "UsernsMode": "",

            "ShmSize": 67108864,

            "Runtime": "runc",

            "ConsoleSize": \[

                0,

                0

            \],

            "Isolation": "",

            "CpuShares": 0,

            "Memory": 0,

            "NanoCpus": 0,

            "CgroupParent": "",

            "BlkioWeight": 0,

            "BlkioWeightDevice": \[\],

            "BlkioDeviceReadBps": null,

            "BlkioDeviceWriteBps": null,

            "BlkioDeviceReadIOps": null,

            "BlkioDeviceWriteIOps": null,

            "CpuPeriod": 0,

            "CpuQuota": 0,

            "CpuRealtimePeriod": 0,

            "CpuRealtimeRuntime": 0,

            "CpusetCpus": "",

            "CpusetMems": "",

            "Devices": \[\],

            "DeviceCgroupRules": null,

            "DeviceRequests": null,

            "KernelMemory": 0,

            "KernelMemoryTCP": 0,

            "MemoryReservation": 0,

            "MemorySwap": 0,

            "MemorySwappiness": null,

            "OomKillDisable": false,

            "PidsLimit": null,

            "Ulimits": null,

            "CpuCount": 0,

            "CpuPercent": 0,

            "IOMaximumIOps": 0,

            "IOMaximumBandwidth": 0,

            "MaskedPaths": \[

                "/proc/asound",

                "/proc/acpi",

                "/proc/kcore",

                "/proc/keys",

                "/proc/latency\_stats",

                "/proc/timer\_list",

                "/proc/timer\_stats",

                "/proc/sched\_debug",

                "/proc/scsi",

                "/sys/firmware"

            \],

            "ReadonlyPaths": \[

                "/proc/bus",

                "/proc/fs",

                "/proc/irq",

                "/proc/sys",

                "/proc/sysrq-trigger"

            \]

        },

        "GraphDriver": {

            "Data": {

                "LowerDir": "/var/lib/docker/overlay2/c122fe199969590a2cd370c3b9acaad534dccc735c876c80320bd4cbdbec775f-init/diff:/var/lib/docker/overlay2/000a5edb9ee543cabaf77570193be0abe5e408931137ac72696579a8b5aec4e3/diff",

                "MergedDir": "/var/lib/docker/overlay2/c122fe199969590a2cd370c3b9acaad534dccc735c876c80320bd4cbdbec775f/merged",

                "UpperDir": "/var/lib/docker/overlay2/c122fe199969590a2cd370c3b9acaad534dccc735c876c80320bd4cbdbec775f/diff",

                "WorkDir": "/var/lib/docker/overlay2/c122fe199969590a2cd370c3b9acaad534dccc735c876c80320bd4cbdbec775f/work"

            },

            "Name": "overlay2"

        },

        "Mounts": \[\],

        "Config": {

            "Hostname": "06fb54229654",

            "Domainname": "",

            "User": "",

            "AttachStdin": false,

            "AttachStdout": false,

            "AttachStderr": false,

            "Tty": false,

            "OpenStdin": false,

            "StdinOnce": false,

            "Env": \[

                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"

            \],

            "Cmd": \[

                "/bin/bash",

                "-c",

                "while true; do echo hello world; sleep 2;done"

            \],

            "Image": "centos",

            "Volumes": null,

            "WorkingDir": "",

            "Entrypoint": null,

            "OnBuild": null,

            "Labels": {

                "org.label-schema.build-date": "20200114",

                "org.label-schema.license": "GPLv2",

                "org.label-schema.name": "CentOS Base Image",

                "org.label-schema.schema-version": "1.0",

                "org.label-schema.vendor": "CentOS",

                "org.opencontainers.image.created": "2020-01-14 00:00:00-08:00",

                "org.opencontainers.image.licenses": "GPL-2.0-only",

                "org.opencontainers.image.title": "CentOS Base Image",

                "org.opencontainers.image.vendor": "CentOS"

            }

        },

        "NetworkSettings": {

            "Bridge": "",

            "SandboxID": "6a06d9813d491f0deb32e6f80bbefadef7260ddf4927acbf34c8ca602e1266a0",

            "HairpinMode": false,

            "LinkLocalIPv6Address": "",

            "LinkLocalIPv6PrefixLen": 0,

            "Ports": {},

            "SandboxKey": "/var/run/docker/netns/6a06d9813d49",

            "SecondaryIPAddresses": null,

            "SecondaryIPv6Addresses": null,

            "EndpointID": "15fce6e45039266f5fb0101aa28b4c2ecdb1dd065fc112d20648857165420fa7",

            "Gateway": "172.17.0.1",

            "GlobalIPv6Address": "",

            "GlobalIPv6PrefixLen": 0,

            "IPAddress": "172.17.0.2",

            "IPPrefixLen": 16,

            "IPv6Gateway": "",

            "MacAddress": "02:42:ac:11:00:02",

            "Networks": {

                "bridge": {

                    "IPAMConfig": null,

                    "Links": null,

                    "Aliases": null,

                    "NetworkID": "54ab25c530a0b4034ce1447464b518b21c6a5a1a9ba28c0569447d388020a427",

                    "EndpointID": "15fce6e45039266f5fb0101aa28b4c2ecdb1dd065fc112d20648857165420fa7",

                    "Gateway": "172.17.0.1",

                    "IPAddress": "172.17.0.2",

                    "IPPrefixLen": 16,

                    "IPv6Gateway": "",

                    "GlobalIPv6Address": "",

                    "GlobalIPv6PrefixLen": 0,

                    "MacAddress": "02:42:ac:11:00:02",

                    "DriverOpts": null

                }

            }

        }

    }

\]

\[root@localhost ~\]\#

