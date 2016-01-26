#Compaction

Compaction is now run on each shard individually.

Finding all shards

	curl -X GET "http://127.0.0.1:5986/_all_dbs"

Finding all the shards for a database

	curl -X GET "http://127.0.0.1:5984/database-name/_shards"

Compacting a shard

	curl -X POST "http://127.0.0.1:5986/shards%2F80000000-ffffffff%2Fdatabase-name.1453473746/_compact" -H "Content-Type:application/json" --user anadmin
