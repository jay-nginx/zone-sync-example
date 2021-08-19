# zone-sync-example

## Testing the configuration via API

```curl -s '127.0.0.1:8080/api/6/stream/zone_sync' | jq```

Expected output:

``{
  "status": {
    "nodes_online": 1,
    "msgs_in": 12,
    "msgs_out": 13,
    "bytes_in": 524,
    "bytes_out": 422
  },
  "zones": {
    "req": {
      "records_total": 2,
      "records_pending": 0
    }
  }
}``

Check from a few different clients to see the "records total" increment. 


## Troubleshooting

- Ensure there is connectivity between the two instances
- Ensure SSL Certificates between the instances are valid
