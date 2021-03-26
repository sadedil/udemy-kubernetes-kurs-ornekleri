# Kubernetes'e Başlarken adlı Udemy kursu için örnek dosyalar

Bu repo'da, Udemy'de hazırladığım **Kubernetes'e Başlarken** kursunda kullanılan örnek dosyaları bulabilirsiniz. Kayıt olmak için [bu linki](https://www.udemy.com/course/kubernetese-baslarken/?referralCode=A2115E4E29667B515210) takip edebilirsiniz.

* [Pod örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/01-pod)
* [Replication Controller örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/02-rc)
* [Service örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/03-svc)
* [Deployment örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/04-dep)
* [Kubectl Komut Örnekleri](#kubectl-ve-minikube-Komutları)

> Tanıtım videosunu izlemek için aşağıdaki görüntüye tıklayabilirsiniz

[![Kubernetes'e Başlarken Tanıtım Videosu](https://user-images.githubusercontent.com/2132971/111875775-898c8500-89ac-11eb-90e0-bf997024324e.png)](https://www.youtube.com/watch?v=3uZDuYts7tI&feature=youtu.be&hd=1 "Kubernetes'e Başlarken Tanıtım Videosu")

## kubectl ve minikube Komutları

### minikube Komutları

`minikube start:` minikube'u başlatır.

`minikube dashboard:` Kubernetes Dashboard'ı lokalde ayağa kaldırır. 

`minikube stop:` minikube'u durdurur.

### kubectl Komutları

`kubectl version:` kubectl versiyonunu gösterir.

`kubectl version --client:` ??

`kubectl run pod1 --image="imaga-name":` İsmi verilen imajdan pod1 adında pod ayağa kaldırır.

`kubectl get node:` Node'ları listeler.

`kubectl get pods:` Pod'ları listeler.

`kubectl port-forward pod1 8080:80:` pod1 adındaki pod'un 8080 portunu sistemi 80 portuna yönlendirir.

`kubectl top pod1:` pod1 ismindeki pod'un kullandığı kaynakları gösterir.

`kubectl top pods:` Pod'ların kullandığı kaynakları gösterir.

`kubectl delete pod pod1:` pod1 ismindeki pod objesini siler.

`kubectl get pods -w:` Pod'ları anlık olarak gösterir. 

`kubectl get pods --all-namespaces:` Tüm namespaces'lerdeki pod'ları listeler.

`kubectl logs pod1:` pod1 isminki pod'un loglarını gösterir. 

`kubectl logs -f pod1:` pod1 ismindeki pod'un loglarını anlık olarak gösterir.

`kubectl apply -f example.yml:` example.yml içerisindeki ayarları uygular. 

`kubectl exec -it pod1 -- bash:` pod1 ismindeki pod'a bağlanır ve shell bağlantısı açar. 

`kubectl run pod1 --image="image-name":` İsmi verilen imajdan pod1 adında pod ayağa kaldırır.

`kubectl get rc:` ReplicationController objelerini listeler.

`kubectl get rc -o wide:` ???

`kubectl config view:` minikube config'lerini listeler. 

`kubectl create ns ns2:` ns2 adında namespace oluşturur. 

`kubectl config set-context minikube --namespace=ns2:` Varsayılen default namespace'inden ns2 isimli namespace'e geçiş yapar.

`kubectl delete ns ns2:` ns2 namespace'ini siler.

`kubectl scale rc rc2 --replicas=1:` rc tipindeki rc2 objenin replika sayısını 1 yapar. 

`kubectl get all:` Ayakta olan tüm objeleri listeler.

`kubectl describe svc service-for-label-1:` service-for-label-1 ismindeki svc objesinin ayrıntılarını verir. 

`kubectl get svc:` Tüm service'leri listeler. 

`kubectl rollout history deploy dep4:` ???

`kubectl get rs:` ReplikaSet'lerini listeler.

`kubectl rollout undo deploy dep4:` dep4 deploy objesinin durumunu bir önceki durumuna getirir. 