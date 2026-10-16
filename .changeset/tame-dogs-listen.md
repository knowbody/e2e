---
'@e2e-dev/mobile': patch
---

Keep healthy engine sessions open on leased devices across worker replacement. After a failed test, a retired worker could drop the device claim. A competing session could then take the device and make later tests fail with "Device is already in use".

Forced worker shutdown and unconfirmed agent-device recording stops still close the engine session. At run end, the engine closes its sessions and the provider releases its device leases.
