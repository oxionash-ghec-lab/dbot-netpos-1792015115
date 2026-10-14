# own-object dependabot updater network-position rig

- `a1` -> `https://169.254.169.254`  :: CONTROL-1 expect proxy 'forbidden' (IMDS literal, in blockedIPs)
- `a2` -> `https://127.0.0.1:9`  :: CONTROL-4 expect RST/connection refused (loopback, closed port)
- `a3` -> `https://192.0.2.1`  :: CONTROL-5 expect DROPPED/timeout (RFC5737 TEST-NET-1, unroutable)
- `a4` -> `https://registry.npmjs.org`  :: CONTROL-6 expect CONNECTED/served (known-good public registry)
- `a5` -> `https://10.0.0.1`  :: ARM re-measure: task#21 saw timeout 2026-06-07
- `a6` -> `https://172.16.0.1`  :: ARM never measured: RFC1918 172.16/12
- `a7` -> `https://192.168.1.1`  :: ARM never measured: RFC1918 192.168/16
