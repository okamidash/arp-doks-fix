# ARP Fix script

This is a Daemonset that will non-destructively update the ARP table when stale neighbours are present. This is to fix a bug present in Cilium on DOKS that doesn't allow for ARP entries to be updated.

The relevant Cilium issue is [here](https://github.com/cilium/cilium/issues/34503), and the fix is [here](https://github.com/cilium/cilium/pull/37725). This is yet to be deploed in DOKS, so this is a solution until then.

## Deployment

```
kubectl apply -f https://raw.githubusercontent.com/okamidash/ARP-DOKS-FIX/main/daemonset.yaml
```