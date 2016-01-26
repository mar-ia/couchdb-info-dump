#Setup

#Configuration
The uuid of all nodes in a cluster must be the same.

#Connecting the cluster

Add the nodes together

	curl -X PUT "http://127.0.0.1:5986/_nodes/nodename@nodeip" -d {} --user anadmin

List what nodes a node is connected to

	curl -X GET "http://127.0.0.1:5984/_membership" --user anadmin

Finishing the setup

	curl -X POST "http://127.0.0.1:5984/_cluster_setup" -H "Content-Type:application/json" -d '{"action":"finish_cluster"}' --user anadmin

You can do this from Fauxton if you prefer a GUI.
