# Descomplicando Kubernetes 

Aqui trago um compilado da minha jornada pelo treinamento da Linuxtips Kubernetes Essentials.

## Conceitos Chaves do k8s

É muito importante saber que a forma como o Kubernetes gerencia os contêineres é um pouco diferente de outros orquestradores, como o Docker Swarm, sobretudo devido ao fato 
de que ele não trata os contêineres diretamente, mas sim através de pods. Abaixo segue os principais conceitos do k8s.

* **Pod:** É o menor objeto do k8s. Pois  o k8s não trabalha com os contêineres diretamente, mas organiza-os dentro de pods, que são abstrações que dividem os mesmos recursos, como endereços, volumes, ciclos de CPU e memória. Um pod pode possuir vários contêineres; 

* **Deployment:** É um dos principais controllers utilizados. O Deployment, em conjunto com o ReplicaSet, garante que determinado número de réplicas de um pod esteja em execução nos nós workers do cluster. Além disso, o Deployment também é responsável por gerenciar o ciclo de vida das aplicações, onde características associadas a aplicação, tais como imagem, porta, volumes e variáveis de ambiente, podem ser especificados em arquivos do tipo yaml ou json para posteriormente serem passados como parâmetro para o kubectl executar o deployment. Esta ação pode ser executada tanto para criação quanto para atualização e remoção do deployment;

* **ReplicaSets:** É um objeto responsável por garantir a quantidade de pods em execução no nó;

* **Services:** É uma forma de você expor a comunicação através de um ClusterIP, NodePort ou LoadBalancer para distribuir as requisições entre os diversos Pods daquele Deployment. Funciona como um balanceador de carga.
