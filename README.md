# ARP Fix script

This is a Daemonset that will non-destructively update the ARP table when stale neighbours are present. This is to fix a bug present in Cilium on DOKS that doesn't allow for ARP entries to be updated.

The relevant Cilium issue is [here](cilium/cilium/34503), and the fix is [here](ilium/cilium/37725). This is yet to be deploed in DOKS, so this is a solution until then.

## Deployment
