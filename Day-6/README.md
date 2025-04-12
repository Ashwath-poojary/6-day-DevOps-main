kubectl get namespace

kubectl get all -n kube-system

kubectl create ns ashwath-ns
kubectl get ns
kubectl get pods
kubectl run test-pod --image nginx --port 80 -n ashwath-ns
kubectl get pods -n ashwath-ns
kubectl delete pod test-pod -n ashwath-ns

git clone https://github.com/Ashwath-poojary/Ashwath-k86-manifestfiles.git
ls
cd Ashwath-k86-manifestfiles
kubectl apply -f rs.yaml
kubectl get pods -n ashwath-ns
kubectl get rs -n ashwath-ns
kubectl describe pod cart-page-rs-c2t8t -n ashwath-ns

kubectl get rs -n ashwath-ns
kubectl delete rs cart-page-rs -n ashwath-ns
kubectl apply -f deployment.yaml -n ashwath-ns
kubectl get deployments -n ashwath-ns
kubectl get pods -o wide -n ashwath-ns

git pull
kubectl apply -f service.yaml -n ashwath-ns
kubectl get svc -n ashwath-ns

snap install helm --classic
kubectl get pods -n monitoring

eksctl delete cluster --name ashwath-cluster

kubectl cluster-info
kubectl get cluster
cd /root/.kube
vi config
