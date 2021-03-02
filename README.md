# Configuration
Estou utilizando a versão **3.7.3 do python** e versão **19.0.3 do pip**  

Necessário definir o diretório do airflow, padrão é `~/airflow`  
`export AIRFLOW_HOME=~/airflow`  

Instalando apache-airflow:  
`pip install apache-airflow`  

Inicializando o banco de dados de metadados:  
`airflow db init`  

Criando um usuário administrador:  
`airflow users create --username username --firstname fname --lastname lname --role Admin --email example@foobar.com`  
Após isto vai pedir para você definir a senha, e escrever ela novamente para confirmar nenhum erro.  

Inicializando o web server na porta 8080:  
`airflow webserver --port 8080`  
Este terminal deve ficar executando o webserver, vá para outro terminal para continuar.  

Nesse novo terminal você também vai precisar indicar a pasta padrão do seu airflow (ao menos que você tenha deixado o default):  
`export AIRFLOW_HOME=~/airflow`  

Scheduler é responsável por monitorar as tarefas e ativar elas assim que elas estiverem prontas para serem inicializadas. Para deixar um scheduler rodando:  
`airflow scheduler`  