# xTom Mirrors issue tracker

This repository, `xtom/mirrors`, is for issues with public mirrors operated by xTom.

Please open an issue here for problems such as:

- an xTom mirror host is unavailable
- downloads are much slower than expected from a region the mirror is meant to serve
- repository metadata or packages appear to be out of sync
- DNS, TLS, routing, or HTTP errors on an xTom mirror

We are not accepting requests for new mirrored repositories at the moment. The mirror servers do not have enough spare disk space, and our maintenance time is limited. For now, we are using that capacity to keep the current mirrors stable.

## Before opening an issue

Please include enough detail for us to reproduce or trace the problem:

- mirror hostname, such as `mirrors.xtom.hk` or `mirrors.xtom.ee`
- affected path, package, ISO, or repository URL
- when you first saw the problem, with timezone
- where you are testing from, including country or region
- network details, such as ISP, ASN, or data center name
- what you expected to happen
- what happened instead
- command output if relevant, such as `curl -I`, `mtr`, `traceroute`, `wget`, `apt`, `dnf`, `yum`, or `pacman`

Please remove passwords, tokens, and private account details from logs before posting.

## Out of scope

Please do not use this repository for:

- requests to add new distros, repositories, ISO archives, or mirror features
- issues with mirrors not operated by xTom
- upstream package bugs
- general Linux package manager support

Issues outside this scope may be closed so we can keep the tracker focused on mirror operations.

## FAQ

### Why are new mirror requests closed?

xTom is not adding extra repositories right now because the mirror servers do not have enough spare disk space. We also have limited maintenance time, so we are focusing on the mirrors we already run.

### I cannot access a mirror. Is the service down?

Not always. xTom mirror services are intended for users in the region where each mirror server is hosted. If you are outside that region, connectivity may be limited.

If the mirror rejects or drops your connection, your source network may have been blocked by our WAF or other security filtering. If you open an issue, please include your source region, ISP or ASN, timestamp, and `mtr` or `traceroute` output.

### Which official distro mirror endpoints point to xTom?

xTom is currently the official mirror behind these endpoints:

| Project | Official endpoint | xTom host |
| --- | --- | --- |
| Debian Hong Kong | `ftp.hk.debian.org/debian` | `mirrors.xtom.hk/debian` |
| Ubuntu Hong Kong | `hk.archive.ubuntu.com/ubuntu` | `mirrors.xtom.hk/ubuntu` |
| Ubuntu Estonia | `ee.archive.ubuntu.com/ubuntu` | `mirrors.xtom.ee/ubuntu` |

### Where is the xTom Mirrors website?

The xTom Mirrors website is at:

https://xtom.com/mirrors/

## Acknowledgements

We thank [USTC LUG](https://lug.ustc.edu.cn/) and [Tsinghua University TUNA Association](https://tuna.moe/) for their help with the maintenance of xTom Mirrors servers.
