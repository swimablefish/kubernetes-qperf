# iperf3 in kubernetes

1. Choose 2 nodes, one is client, the other is server
2. Put client.yaml into to client's /etc/kubernetes/manifests
3. Put server.yaml into to server's /etc/kubernetes/manifests
4. Install iperf3 into the client and server pods 
5. Run `kubectl create -f svc.yaml`
6. Run `iperf3 -p 5001 -s` in the server pod
7. Run `iperf3 -p 5001 -t 10 -p 10` in the client pod to start the test
