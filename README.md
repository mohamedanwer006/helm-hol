# Helm app

#### Start by containerize the application https://github.com/tradebyte/DevOps-Challenge

```
└─ mohamed@DevOps:$ docker push mohameddev006/web-app:v5

```

### Create helm chart

```
helm create web-app
```

### run chart on minikube

```
helm install webapp ./web-app
```

![alt](./assets/1.png)

### Test the application

![alt](./assets/test.png)

### Clean up

```
helm delete webapp
```

## index an deploy chart to github pages 

### package the chart

```
helm package . -d charts

```
### index

```
helm repo index charts
```

> push code to gh-pages branch to act as a repo for the chart

### Test
```
helm repo add mohamed  https://mohamedanwer006.github.io/helm-hol/charts

```
 ![alt](./assets/2.png)

### Create metadata file to gVerified Publisher  on artifact.io

![alt](./assets/3.png)

![alt](./assets/4.png)

---

## Deploy jenkins 

### Add repo
```
helm repo add jenkins https://charts.jenkins.io
helm repo update
```
### install jenkins

```
helm install jenkins jenkins/jenkins
```

### output
![alt](./assets/6.png)

![alt](./assets/5.png)

