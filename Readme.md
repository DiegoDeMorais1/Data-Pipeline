## Principais conceitos do Airflow
<div align="center">
  <a href="https://www.linkedin.com/in/diego-canquerini-350a6a206/" target="_blank">
    <img src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="https://github.com/DiegoDeMorais1">
  <img src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white"></a>
  <a href="https://www.python.org/">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54"></a>
  <a href="https://www.apache.org/">
    <img src="https://img.shields.io/badge/apache-%23D42029.svg?style=for-the-badge&logo=apache&logoColor=white"><img</a>
  </a>
</div>
    

Na internet, existem diversas APIs que trazem informações climáticas sobre diferentes lugares do mundo e nós utilizaremos uma delas, a Visualcrossing. Vamos acessar o site (https://www.visualcrossing.com) 

| :placard: Vitrine.Dev |     |
| -------------  | --- |
| :sparkles: Nome        | **Data pipeline Chuvas**
| :label: Tecnologias | Python, Apache Airflow, VSCode, Linux  (tecnologias utilizadas)
| :fire: Desafio     |  https://cursos.alura.com.br/course/apache-airflow-primeiro-pipeline-dados

O Airflow organiza seus fluxos de trabalho em DAGs, que são basicamente pipelines de dados definidos utilizando a linguagem Python. Cada DAG é composto por um conjunto de tarefas que são utilizadas para implementar uma determinada lógica no pipeline. Sendo que cada tarefa é definida pela instância de um operador.
De forma resumida, os principais conceitos do Airflow são:

 DAG: fluxo de trabalho definido em Python.
 Task: unidade mais básica de um DAG.
 Operator: encapsula a lógica para fazer uma unidade de trabalho (task).

DAG é uma abreviação para “Directed Acyclic Graphs” - Grafos Acíclicos Dirigidos, em tradução livre - sendo que cada uma dessas palavras significa:

 Grafos: ferramenta matemática na qual há nós e arestas responsáveis por conectar esses nós;
 Direcionado: indica que o fluxo de trabalho se dá apenas em uma direção; e
 Acíclico: significa que a execução não entrará em um laço de repetição. Então, eventualmente, acabaremos em um nó final que não estará conectado com o nó inicial.

***
<p align="center">
  <img alt="Aiflow" src="Aula2-img1.png">
O Airflow possui 4 componentes principais que devem estar em execução para que ele funcione corretamente. São eles o web server, scheduler, banco de dados e executor.

O web server é um servidor feito em Flask, um framework web Pyhton, que serve para nos apresentar a interface de usuário do Airflow, portanto, é por meio dele que acessamos esta interface.

O scheduler ("agendador" em português) é responsável pelo agendamento da execução das tarefas dos DAGs, então ele determina quais tarefas serão realizadas, onde serão executadas e em qual ordem isso acontecerá.

O banco de dados, por sua vez, serve para armazenar todos os metadados referentes aos DAGs. Sendo assim, ele registra o horário em que as tarefas foram executadas, quanto tempo cada task levou para ser realizada e o estado de cada uma - se foram executadas com sucesso ou falha, e outras informações relacionadas.

Por fim, temos o executor, que é o mecanismo de execução das tarefas. Ou seja, ele é responsável por descobrir quais recursos serão necessários para executar essas tasks.

*Tarefas a serem feitas:

   precisa ser executado toda segunda-feira;
   criar pastas de armazenamento de dados;
   extrair dados da previsão do tempo referente à semana de execução.

    cd airflowalura/
    source venv/bin/activate
    export AIRFLOW_HOME=~/Documentos/datapipeline2/airflowalura 
    airflow standalone
