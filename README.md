

- https://developer.hashicorp.com/vault/docs
- https://hub.docker.com/r/hashicorp/vault
- https://developer.hashicorp.com/vault/docs/concepts/ha
- https://developer.hashicorp.com/vault/tutorials/raft/raft-storage
- https://developer.hashicorp.com/vault/docs/configuration
- https://github.com/hashicorp/vault
- https://developer.hashicorp.com/vault/docs/concepts/seal
- https://developer.hashicorp.com/vault/tutorials/auto-unseal/autounseal-transit
- https://stackoverflow.com/questions/75716087/does-vault-seal-itself-in-ha
- https://github.com/hashicorp-education/learn-vault-raft/blob/main/raft-storage/local/cluster.sh#L349

```
docker run --cap-add=IPC_LOCK -d --name=dev-vault hashicorp/vault

docker run --cap-add=IPC_LOCK -e 'VAULT_LOCAL_CONFIG={"storage": {"file": {"path": "/vault/file"}}, "listener": [{"tcp": { "address": "0.0.0.0:8200", "tls_disable": true}}], "default_lease_ttl": "168h", "max_lease_ttl": "720h", "ui": true}' -p 8200:8200 hashicorp/vault server
```

  
