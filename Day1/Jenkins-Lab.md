# Jenkins

## Day1

## 1- install jenkins with docker image

```bash
docker run -p 8008:8080 -d --name jenkins jenkins/jenkins:lts
```

## 2- install role based authorization plugin

![Lab2-2 q1.png](./screenshots/day-1-q2.png "Lab2-2 q1.png")

## 3- create new user

## 4- create read role and assign it to the new user

![Lab2-2 q1.png](./screenshots/day-1-q3.png "Lab2-2 q1.png")

## 5- create free style pipeline and link it to private git repo(inside it create directory and create file with "hello world")

![Lab2-2 q1.png](./screenshots/day-1-q5.png "Lab2-2 q1.png")

---

## 1- create declarative in jenkins GUI pipeline for your own repo to do "ls"

![Lab2-2 q1.png](./screenshots/day-1-q6.png "Lab2-2 q1.png")

## 2- create scripted in jenkins GUI pipeline for your own repo to do "ls"

![Lab2-2 q1.png](./screenshots/day-1-q7.png "Lab2-2 q1.png")

## 3- create the same with jenkinsfile in your branches as multibranch pipeline

![Lab2-2 q1.png](./screenshots/day-1-q8-1.png "Lab2-2 q1.png")
![Lab2-2 q1.png](./screenshots/day-1-q8-2.png "Lab2-2 q1.png")
![Lab2-2 q1.png](./screenshots/day-1-q8-3.png "Lab2-2 q1.png")

---

