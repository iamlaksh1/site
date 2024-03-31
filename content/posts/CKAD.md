---
title: "K8s - CKAD Exam Tips and Notes"
date: "2024-02-14" 
tags:
  - "gis"
  - "k8s"
  - "CKAD"
  - "Linux"
  - "career"
  - "Devops"
  - "cheatsheet"
  - "tips"
---

The CKAD exam is about more than just your knowledge of Kubernetes. It also tests your ability to complete tasks quickly. Speed ​​and efficiency are key to passing this test. This exam truly tests the pratical working knowledge and your proficiency.

Please read the [important instructions](https://docs.linuxfoundation.org/tc-docs/certification/tips-cka-and-ckad) about device you use for taking exam, protocor requirements, exam details etc 

### Few Tips :

1. Please run [PSI Online Proctoring System Check](https://syscheck.bridge.psiexams.com/) before the exam to ensure no surprises on exam day. Please un-install old version (if any , used for other exam) and re-install latest one.

2. [Understand exam UI](https://2145393087-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-M5QaeeC1mG9VndIpgJe%2Fuploads%2F13joD9D4ULTjRYNMP1eY%2FLF%20Remote%20Desktop%20070722d.png?alt=media&token=3784c329-768e-475c-b852-88ef98c899ce) - this is makes thing easy and gives some familarity 

3. Proctor is so strict; they ask you to show the entire room, walls, ceiling, under the table , mouse pad etc. Please be patient and do not get annoyed, this is their job and must needed one.

4. Keep a proper valid identification document  as per requirement. 

5.  **Important tip** Though the exam is open book, means you can use kubernetes.io docs for reference, it will be time consuming if you are not familiar with commands or usage. Searching the doc should be your last option 

6. **DO NOT PANIC** in case of techincal issue or system issue, PSI online system has certain gotchas, proctor chat will help you or you can write to linux foundation and get this sorted out. Dont think too much. 

7. Pratice the mock /simulator exams in device you are planning to take. If you are habituated to use big dual screens for study and prep, during exam if you use 14'' laptop (*dual screens not permitted*); your mind needs some realignment on fonts/size. So please be prepared.

8. Please charge your device to 100% and keep charger connected. 

9. ***Unpopular opinion***: Just going through popular udemy course and doing the lab on each topic will NOT be sufficient. Ensure you get HIGH score on those simulator (***killer.sh***) in a **GIVEN TIME**. This is important for your success.


10. Technical tips:
    - Set up most commonly needed commands in alias will be such a time saver
    - Do not waste your time on YAML alignment.
    - Please familairize with VIM or Nano . Especially copy-paste from browser.
    - Check the each task *weightage* and work accordingly.
    - If you copy paste from browser to terminal, alignment will go for the toss. Please ensure you Setup VIM (tabstop, expandtab, shiftwidth) and it's much easier
    -  Don't overthink the question. If you're not making progress or stuck on a question for more than 5 minutes, mark it and come back to it later
    - Understand the question and context before you start the command. Some of them were tricky and worded to confuse you.
    - Make sure to run the command they give you at the beginning of each question to set the context. Check out this [video](https://www.youtube.com/watch?v=9UqkWcdy140) from the Linux Foundation that demonstrates it. Then, if the query tells you to run in a specific namespace, use the *kn* alias to specify the namespace so you can pass the namespace into commands. If it doesn't specify a namespace, run *kn* default to make sure you're in the default namespace.
    
### Some tid-bits  

1. Make sure if spec is at container level or POD level. 
1. Always take a back-up of given manifest before you edit/modify original file
1. Never delete any resources (or take a backup of resources) from cluster, unless asked for. 
1. Services match a set of Pods using labels and selectors
1. Network Policies are additive, so you can have multiple policies targeting a particular Pod. The sum of the “allow” rules from all the policies will apply. Traffic from or to sources that don’t match any of the “allow” rules will be blocked if the target Pod is also covered by a “deny” policy
1. Learn how to inject `ConfigKeyMap` as environment variables and also mounted as volume
1.  `-A` used to get resources from the all the namespaces (--all-namespaces); `-O` represents output format (--output)
1. `-p` represents "previous" (--previous) ;  `-it` represents run a container in an interactive mode ; `-- wget` to run wget command inside an container ; ` -- wget -O- ` print the ouput in standard output (STDOUT)
1.  run a command inside container `command: ['sh','-c','echo "check this out!" > /tmp/web-content/index.html']`
1. Understand the security context; previleges, `runAsUser` (*0 for root*) ; is it for pod or container?
1. Blue/green stratergy can be implemented easily by updating selector on service to new one (label for new version)
1. At any given time, only a single `PersistentVolumeClaim` can be bound to a `PersistentVolume` . The accessModes of the claim or volume so that they match. Else claim will be in pending status.
1. The default Service Type is `ClusterIP`; however, to bind a Pod to a port in a Node, we need to use use a Service of type `NodePort`. Always use `LoadBalancer` as a type for external access.
1. In order to diagnose pod failures - adding `terminationMessagePath` will increase the context available when debugging the failure.
1. `LivenessProbe` will be automatically restart the container if it fails.
1. Note down abbrevations : RWO, ROX, RWX, RWOP -- X stands for Many ; ReadWriteOncePod (RWOP)
1. To be update labels of pod in bulk with condition `kubectl label pod -l "app in(v1,v2)" tier=web` 
1. Understanding `ingress` and `egress` rules , path, ports (exclusion and inclusion of certain path is important)
1. Pratice to create mult-pod container using imperative command (with little bit of editing) saves some time.
1. If question says, `root of mounted volume` means - find the root path ; if volume-name is `web-content` then use mount path may be `/tmp/web-content` 
1. use `nodeSelector` to run the pod on dedicated node (here - controlplane) ex: 
     ```
        nodeSelector:
           kubernetes.io/hostname: controlplane
     ```
1. If the task is not completed within 20 seconds the job should fail and pods should be terminated. use `activeDeadlineSeconds`
1. How to create cron-job schedule - every 1 min, every 10 minutes, weekly once, monthly once, every friday etc.
1. Understand difference between Ports, TargetPort , Node Ports . This is super important.
1. How to create an deployment using pod template with additional features.
1. How to create cron-job and then create a job
1. API depreciation, how to upgrade the existing object from older depreciated version to new 
1. The Metrics Sever's frequency of metrics collections is not fast enough for accurate resource usage metrics
1. The securityContext.runAsUser field can be used to set the user ID for the container's process, not to grant access to network storage devices. Capablities can be added at container level. 
1. Pratice how to take a back up of ETCD database (needs etcd-client) and certificates
1. Learn about docker fundamentals, how to create a image and container and push to registry and export the image as tar and save etc
1. There are 5 volumes types :  emptyDir, hostPath, configMap, secret, Nfs , cloud provider solution
1. Once a Secret or `ConfigMap` is marked as immutable, it is not possible to revert this change nor to mutate the contents of the data field. You can only delete and recreate the Secret. Existing Pods maintain a mount point to the deleted Secret - it is recommended to recreate these pods.
1. Unlike virtual machines containers are not completely isolated
from their host. Containers and the hosts share the same kernel. Containers are
isolated using namespaces in Linux. The host has a namespace and the containers
have their own namespace. All the processes run by the containers are in fact run on
the host itself, but in their own namespaces.
### [Domains & Competencies with %](https://training.linuxfoundation.org/certification/certified-kubernetes-application-developer-ckad/) 

1. Application Design and Build - 20%
2. Application Design and Build - 20%
3. Application Deployment- 20%
4. Application Observablity and Maintenance - 15%
5. Application Environment, Configuration and Security - 25%

### Frequently Used Commands

kubectl with k alias and Bash autocompletion - Preconfigured 

curl and wget is pre-installed and configured 

js, tmux, man and manager readily available 

####  Helpful alias which are frequently needed 

```shell script
 
alias kn='kubectl config set-context --current --namespace '

# to force delete 
export now='--grace-period=0 --force'  
    
 # Env Variable
export do='--dry-run=client -o yaml'
```



| Description | Command |
| --- | --- |    
| Set namespace preference             | `kn <namespace-name>`    
| Create pod manifest and save         | `kubectl run nginx --image=nginx $do > nginx-pod.yaml` 
| List all resources                      | `kubectl get all --all-namespaces`  
| List pods with nodes info            | `kubectl get pod -o wide`              
| Run nginx pod and expose it          | `kubectl run my-nginx --restart=Never --image=nginx --port=80 --expose`                   
| create deplpoyment with 4 replica    | `kubectl create deployment nginx --image=nginx --replicas=4` 
| set the node named <worker node> as unavailable and reschedule all the pods running on it | ` Kubectl drain node <worker node> --ignore-daemonsets` 
|Create secrete with 2 sets of key value pairs | `kubectl create secret generic my-secret --from-literal=key1=supersecret --from-literal=key2=topsecret`
| echo to base64 format | `echo -n "value" \| base64 `
| echo to decode base64 format | `echo -n "value" \| base64 --decode `
| Pod with service creation | `kubectl run echoserver --image=nginx --restart=Never --port=8080 --expose `
| Deployment with service creation | `kubectl create deployment echoserver --image=nginx --replicas=5` `kubectl expose deployment echoserver --port=80 --target-port=8080`                           
                     


