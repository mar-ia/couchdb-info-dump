#Views

The query parameter `update_seq` is removed as it does not work in a cluster.
You can no longer query the view with `update_seq=true` and use the
`update_seq` in the responce as the starting point in a changes feed using the
`since` parameter.
