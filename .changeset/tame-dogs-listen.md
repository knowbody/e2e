---
'@e2e-dev/mobile': patch
---

Keep provider-owned agent-device sessions open across worker replacement. The run still closes each session and releases each device lease when it ends.
