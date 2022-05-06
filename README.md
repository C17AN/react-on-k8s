## 🔨 K8s에 컨테이너화된 프론트엔드 어플리케이션 배포 예제

### Steps

1. `yarn build` 로 리액트 빌드 후, `docker build -t <도커허브 아이디>/<이미지 이름> .` 으로 이미지를 빌드합니다.
2. 이미지를 도커허브 등의 레포지토리에 배포합니다.
3. `k8s` 폴더로 이동 후, `deployment.yaml` 및 `load-balancer.yaml` 템플릿을 적용합니다.
4. 프로비저닝이 완료되면 `minikube ip` 로 아이피 확인 후, `http://<미니쿠베 아이피>:31000` 포트에 배포된 것을 확인할 수 있습니다.

> 만약 M1 칩 기반 맥북을 사용한다면 포트포워딩을 추가로 수행해야 합니다. [(참고 : 깃허브 이슈)](https://github.com/kubernetes/minikube/issues/9016)
>
> 해당 경우, `kubectl port-forward service/load-balancer <로컬 포트>:80` 으로 포트포워딩을 수행한 후, `localhost:<포트포워딩한 로컬 포트>` 에서 결과물을 확인할 수 있습니다.

### 추가 과제

- 이제 만약 개발 팀에서 소스를 수정한다면, 어떻게 수정된 소스를 컨테이너에 반영할 수 있을끼? []
