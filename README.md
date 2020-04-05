# This a repo to demostrate my CKAD Cert practice


# Understand Kubernetes API Primitives

## Pods

## Services

Say you got a frontend web server and a backend database server. There may be multiple pods that all act as the frontend, but there may only be a single backend database pod. You need to solve two problems to make the system function:

	* External clients need to connect to the frontend pods without caring if there’s
	only a single web server or hundreds.
	
	* The frontend pods need to connect to the backend database. Because the database
	runs inside a pod, it may be moved around the cluster over time, causing
	its IP address to change. You don’t want to reconfigure the frontend pods every
	time the backend database is moved.
