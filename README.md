## π¨ K8sμ μ»¨νμ΄λνλ νλ‘ νΈμλ μ΄νλ¦¬μΌμ΄μ λ°°ν¬ μμ 

### Steps

1. `yarn build` λ‘ λ¦¬μ‘νΈ λΉλ ν, `docker build -t <λμ»€νλΈ μμ΄λ>/<μ΄λ―Έμ§ μ΄λ¦> .` μΌλ‘ μ΄λ―Έμ§λ₯Ό λΉλν©λλ€.
2. μ΄λ―Έμ§λ₯Ό λμ»€νλΈ λ±μ λ ν¬μ§ν λ¦¬μ λ°°ν¬ν©λλ€.
3. `k8s` ν΄λλ‘ μ΄λ ν, `deployment.yaml` λ° `load-balancer.yaml` ννλ¦Ώμ μ μ©ν©λλ€.
4. νλ‘λΉμ λμ΄ μλ£λλ©΄ `minikube ip` λ‘ μμ΄νΌ νμΈ ν, `http://<λ―ΈλμΏ λ²  μμ΄νΌ>:31000` ν¬νΈμ λ°°ν¬λ κ²μ νμΈν  μ μμ΅λλ€.

> λ§μ½ M1 μΉ© κΈ°λ° λ§₯λΆμ μ¬μ©νλ€λ©΄ ν¬νΈν¬μλ©μ μΆκ°λ‘ μνν΄μΌ ν©λλ€. [(μ°Έκ³  : κΉνλΈ μ΄μ)](https://github.com/kubernetes/minikube/issues/9016)
>
> ν΄λΉ κ²½μ°, `kubectl port-forward service/load-balancer <λ‘μ»¬ ν¬νΈ>:80` μΌλ‘ ν¬νΈν¬μλ©μ μνν ν, `localhost:<ν¬νΈν¬μλ©ν λ‘μ»¬ ν¬νΈ>` μμ κ²°κ³Όλ¬Όμ νμΈν  μ μμ΅λλ€.

### μΆκ° κ³Όμ 

- μ΄μ  λ§μ½ κ°λ° νμμ μμ€λ₯Ό μμ νλ€λ©΄, μ΄λ»κ² μμ λ μμ€λ₯Ό μ»¨νμ΄λμ λ°μν  μ μμλΌ? []
