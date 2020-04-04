https://cloud.mongodb.com/v2/5e883d9adf26162d6e9c774d#clusters/connect?clusterId=Cluster0



```
$ mongo "mongodb+srv://cluster0-mmmko.mongodb.net/test"  --username [username]
MongoDB shell version v4.2.5
Enter password: 
connecting to: mongodb://cluster0-shard-00-00-mmmko.mongodb.net:27017,cluster0-shard-00-02-mmmko.mongodb.net:27017,cluster0-shard-00-01-mmmko.mongodb.net:27017/test?authSource=admin&compressors=disabled&gssapiServiceName=mongodb&replicaSet=Cluster0-shard-0&ssl=true
2020-04-04T21:16:44.831+0900 I  NETWORK  [js] Starting new replica set monitor for Cluster0-shard-0/cluster0-shard-00-00-mmmko.mongodb.net:27017,cluster0-shard-00-02-mmmko.mongodb.net:27017,cluster0-shard-00-01-mmmko.mongodb.net:27017
2020-04-04T21:16:44.832+0900 I  CONNPOOL [ReplicaSetMonitor-TaskExecutor] Connecting to cluster0-shard-00-00-mmmko.mongodb.net:27017
2020-04-04T21:16:44.832+0900 I  CONNPOOL [ReplicaSetMonitor-TaskExecutor] Connecting to cluster0-shard-00-01-mmmko.mongodb.net:27017
2020-04-04T21:16:44.832+0900 I  CONNPOOL [ReplicaSetMonitor-TaskExecutor] Connecting to cluster0-shard-00-02-mmmko.mongodb.net:27017
2020-04-04T21:16:49.277+0900 I  NETWORK  [ReplicaSetMonitor-TaskExecutor] Confirmed replica set for Cluster0-shard-0 is Cluster0-shard-0/cluster0-shard-00-00-mmmko.mongodb.net:27017,cluster0-shard-00-01-mmmko.mongodb.net:27017,cluster0-shard-00-02-mmmko.mongodb.net:27017
Implicit session: session { "id" : UUID("0c26a55f-a562-4d2f-88c3-5198a3f97a39") }
MongoDB server version: 4.2.5
Welcome to the MongoDB shell.
For interactive help, type "help".
For more comprehensive documentation, see
	http://docs.mongodb.org/
Questions? Try the support group
	http://groups.google.com/group/mongodb-user
MongoDB Enterprise Cluster0-shard-0:PRIMARY> db.version()
4.2.5
MongoDB Enterprise Cluster0-shard-0:PRIMARY> db.serverStatus().storageEngine
{
	"name" : "wiredTiger",
	"supportsCommittedReads" : true,
	"oldestRequiredTimestampForCrashRecovery" : Timestamp(1586002658, 1),
	"supportsPendingDrops" : true,
	"dropPendingIdents" : NumberLong(0),
	"supportsSnapshotReadConcern" : true,
	"readOnly" : false,
	"persistent" : true,
	"backupCursorOpen" : false
}
MongoDB Enterprise Cluster0-shard-0:PRIMARY> rs.status()
{
	"set" : "Cluster0-shard-0",
	"date" : ISODate("2020-04-04T12:18:12.448Z"),
	"myState" : 1,
	"term" : NumberLong(2),
	"syncingTo" : "",
	"syncSourceHost" : "",
	"syncSourceId" : -1,
	"heartbeatIntervalMillis" : NumberLong(2000),
	"majorityVoteCount" : 2,
	"writeMajorityCount" : 2,
	"optimes" : {
		"lastCommittedOpTime" : {
			"ts" : Timestamp(1586002684, 2),
			"t" : NumberLong(2)
		},
		"lastCommittedWallTime" : ISODate("2020-04-04T12:18:04.882Z"),
		"readConcernMajorityOpTime" : {
			"ts" : Timestamp(1586002684, 2),
			"t" : NumberLong(2)
		},
		"readConcernMajorityWallTime" : ISODate("2020-04-04T12:18:04.882Z"),
		"appliedOpTime" : {
			"ts" : Timestamp(1586002684, 2),
			"t" : NumberLong(2)
		},
		"durableOpTime" : {
			"ts" : Timestamp(1586002684, 2),
			"t" : NumberLong(2)
		},
		"lastAppliedWallTime" : ISODate("2020-04-04T12:18:04.882Z"),
		"lastDurableWallTime" : ISODate("2020-04-04T12:18:04.882Z")
	},
	"lastStableRecoveryTimestamp" : Timestamp(1586002658, 1),
	"lastStableCheckpointTimestamp" : Timestamp(1586002658, 1),
	"electionCandidateMetrics" : {
		"lastElectionReason" : "priorityTakeover",
		"lastElectionDate" : ISODate("2020-04-03T11:45:34.004Z"),
		"electionTerm" : NumberLong(2),
		"lastCommittedOpTimeAtElection" : {
			"ts" : Timestamp(1585914328, 1),
			"t" : NumberLong(1)
		},
		"lastSeenOpTimeAtElection" : {
			"ts" : Timestamp(1585914328, 1),
			"t" : NumberLong(1)
		},
		"numVotesNeeded" : 2,
		"priorityAtElection" : 7,
		"electionTimeoutMillis" : NumberLong(5000),
		"priorPrimaryMemberId" : 0,
		"numCatchUpOps" : NumberLong(0),
		"newTermStartDate" : ISODate("2020-04-03T11:45:34.159Z"),
		"wMajorityWriteAvailabilityDate" : ISODate("2020-04-03T11:45:34.473Z")
	},
	"electionParticipantMetrics" : {
		"votedForCandidate" : true,
		"electionTerm" : NumberLong(1),
		"lastVoteDate" : ISODate("2020-04-03T11:45:27.897Z"),
		"electionCandidateMemberId" : 0,
		"voteReason" : "",
		"lastAppliedOpTimeAtElection" : {
			"ts" : Timestamp(0, 0),
			"t" : NumberLong(-1)
		},
		"maxAppliedOpTimeInSet" : {
			"ts" : Timestamp(1585914322, 1),
			"t" : NumberLong(-1)
		},
		"priorityAtElection" : 7
	},
	"members" : [
		{
			"_id" : 0,
			"name" : "cluster0-shard-00-00-mmmko.mongodb.net:27017",
			"health" : 1,
			"state" : 2,
			"stateStr" : "SECONDARY",
			"uptime" : 88369,
			"optime" : {
				"ts" : Timestamp(1586002684, 2),
				"t" : NumberLong(2)
			},
			"optimeDurable" : {
				"ts" : Timestamp(1586002684, 2),
				"t" : NumberLong(2)
			},
			"optimeDate" : ISODate("2020-04-04T12:18:04Z"),
			"optimeDurableDate" : ISODate("2020-04-04T12:18:04Z"),
			"lastHeartbeat" : ISODate("2020-04-04T12:18:11.108Z"),
			"lastHeartbeatRecv" : ISODate("2020-04-04T12:18:10.750Z"),
			"pingMs" : NumberLong(0),
			"lastHeartbeatMessage" : "",
			"syncingTo" : "cluster0-shard-00-01-mmmko.mongodb.net:27017",
			"syncSourceHost" : "cluster0-shard-00-01-mmmko.mongodb.net:27017",
			"syncSourceId" : 1,
			"infoMessage" : "",
			"configVersion" : 2
		},
		{
			"_id" : 1,
			"name" : "cluster0-shard-00-01-mmmko.mongodb.net:27017",
			"health" : 1,
			"state" : 1,
			"stateStr" : "PRIMARY",
			"uptime" : 88408,
			"optime" : {
				"ts" : Timestamp(1586002684, 2),
				"t" : NumberLong(2)
			},
			"optimeDate" : ISODate("2020-04-04T12:18:04Z"),
			"syncingTo" : "",
			"syncSourceHost" : "",
			"syncSourceId" : -1,
			"infoMessage" : "",
			"electionTime" : Timestamp(1585914334, 1),
			"electionDate" : ISODate("2020-04-03T11:45:34Z"),
			"configVersion" : 2,
			"self" : true,
			"lastHeartbeatMessage" : ""
		},
		{
			"_id" : 2,
			"name" : "cluster0-shard-00-02-mmmko.mongodb.net:27017",
			"health" : 1,
			"state" : 2,
			"stateStr" : "SECONDARY",
			"uptime" : 88369,
			"optime" : {
				"ts" : Timestamp(1586002684, 2),
				"t" : NumberLong(2)
			},
			"optimeDurable" : {
				"ts" : Timestamp(1586002684, 2),
				"t" : NumberLong(2)
			},
			"optimeDate" : ISODate("2020-04-04T12:18:04Z"),
			"optimeDurableDate" : ISODate("2020-04-04T12:18:04Z"),
			"lastHeartbeat" : ISODate("2020-04-04T12:18:12.357Z"),
			"lastHeartbeatRecv" : ISODate("2020-04-04T12:18:10.452Z"),
			"pingMs" : NumberLong(1),
			"lastHeartbeatMessage" : "",
			"syncingTo" : "cluster0-shard-00-01-mmmko.mongodb.net:27017",
			"syncSourceHost" : "cluster0-shard-00-01-mmmko.mongodb.net:27017",
			"syncSourceId" : 1,
			"infoMessage" : "",
			"configVersion" : 2
		}
	],
	"ok" : 1,
	"$clusterTime" : {
		"clusterTime" : Timestamp(1586002684, 2),
		"signature" : {
			"hash" : BinData(0,"SWHMJHC6ThuIJTjlfZZAS+wuZL8="),
			"keyId" : NumberLong("6811450168722849795")
		}
	},
	"operationTime" : Timestamp(1586002684, 2)
}
```
