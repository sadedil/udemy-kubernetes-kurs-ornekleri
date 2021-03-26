# Kubernetes'e Başlarken adlı Udemy kursu için örnek dosyalar

Bu repo'da, Udemy'de hazırladığım **Kubernetes'e Başlarken** kursunda kullanılan örnek dosyaları bulabilirsiniz. Kayıt olmak için [bu linki](https://www.udemy.com/course/kubernetese-baslarken/?referralCode=A2115E4E29667B515210) takip edebilirsiniz.

* [Pod örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/01-pod)
* [Replication Controller örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/02-rc)
* [Service örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/03-svc)
* [Deployment örnekleri](https://github.com/sadedil/udemy-kubernetes-kurs-ornekleri/tree/main/04-dep)
* [Kurs içerisinde kullanılan `kubectl` ve `minikube` komutları](#kurs-içerisinde-kullanılan-kubectl-ve-minikube-komutları)

> Tanıtım videosunu izlemek için aşağıdaki görüntüye tıklayabilirsiniz

[![Kubernetes'e Başlarken Tanıtım Videosu](https://user-images.githubusercontent.com/2132971/111875775-898c8500-89ac-11eb-90e0-bf997024324e.png)](https://www.youtube.com/watch?v=3uZDuYts7tI&feature=youtu.be&hd=1 "Kubernetes'e Başlarken Tanıtım Videosu")

## Kurs içerisinde kullanılan `kubectl` ve `minikube` komutları

### `minikube` komutları

`minikube start`: _minikube_'u başlatır.

`minikube dashboard`: _minikube_ içerisinde çalışan _Kubernetes Dashboard_ _pod_'unu, _port-forward_ ile kendi bilgisyarınızdan erişebilir hale getirir.

`minikube stop`: _minikube_'u durdurur.

`minikube status`: _minikube_'un durumunu gösterir.

### `kubectl` komutları

`kubectl version`: _kubectl_ aracının kendi versiyon bilgisini ve o anda bağlı olduğu _cluster_'ın versiyon bilgisini gösterir.

`kubectl version --client`: _kubectl_ aracının kendi versiyon bilgisini gösterir.

`kubectl run pod1 --image="imaga-name"`: İsmi verilen imajdan pod1 adında pod ayağa kaldırır.

`kubectl get node`: _Node_'ları listeler.

`kubectl get pods`: _Pod_'ları listeler.

`kubectl port-forward pod1 8080:80`: _pod1_ adındaki _pod_'un _80_ portunu kendi bilgisayarınızdaki _8080_ portuna yönlendirir.

`kubectl delete pod pod1`: _pod1_ ismindeki _pod_ objesini siler.

`kubectl get pods -w`: _Pod_'ları listeler ve izleme modunu başlatır, herhangi bir değişiklik olduğunda anlık olarak gösterir (`-w` ya da `--watch` birçok _kubectl_ komutu ile birlikte kullanılabilir).

`kubectl get pods --all-namespaces`: Tüm _namespace_'lerdeki _pod_'ları listeler (`--all-namespaces` birçok _kubectl_ komutu ile birlikte çalışır).

`kubectl logs pod1`: _pod1_ isminki _pod_'un loglarını gösterir. 

`kubectl logs -f pod1`: _pod1_ ismindeki _pod_'un loglarını anlık olarak gösterir (`-f` ya da `--follow` kullanılabilir).

`kubectl apply -f example.yml`: _example.yml_ içerisindeki yönergeleri uygular. 

`kubectl exec -i -t pod1 -- bash`: _pod1_ ismindeki _pod_'a bağlanır ve _bash_ _shell_'ini açar. 

`kubectl run pod1 --image="image-name"`: İsmi verilen imajdan _pod1_ adında _pod_ ayağa kaldırır.

`kubectl get rc`: _ReplicationController_ objelerini listeler.

`kubectl get rc -o wide`: _ReplicationController_ objelerini listeler ekstra birkaç kolon bilgisi daha ekleyerek gösterir (`-o wide` ya da `--output wide` birden çok _kubectl_ komutu ile birlikte kullanılabilir)

`kubectl config view`: _kubeconfig_ dosyasının içeriğini listeler.

`kubectl create ns ns2`: _ns2_ adında namespace oluşturur. 

`kubectl config set-context minikube --namespace=ns2`: O anda bulunulan _context_'i ve _namespace_'i değiştirir. Bu örnekte _minikube_ _context_'i içerisindeki _ns2_ _namespace_'ine geçiş gösterilmiştir.

`kubectl delete ns ns2`: _ns2_ _namespace_'ini siler.

`kubectl scale rc rc2 --replicas=1`: _rc2_ isimli _ReplicationController_'daki _replica_ (kopya) sayısını 1'e ölçekler.

`kubectl get all`: Geçerli olan _namespace_ içerisindeki tüm _Kubernetes_ objelerini listeler.

`kubectl describe svc service-for-label-1`: _service-for-label-1_ ismindeki _service_ objesinin ayrıntılarını verir. 

`kubectl get svc`: Tüm _service_'leri listeler. 

`kubectl rollout history deploy dep4`: _dep4_ isimli _Deployment_ objesi üzerindeki güncelleme durumunu gösterir

`kubectl get rs`: _ReplicaSet_'leri listeler.

`kubectl rollout undo deploy dep4`: _dep4_ isimli _Deployment_ objesini, bir önceki sürüme getirir (_rollback_)

## Repo'ya katkı verenler

- [akiffeyzioglu](https://github.com/akiffeyzioglu)
