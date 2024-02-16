# AI900 🤖
## - Ao iniciar o Estúdio de aprendizagem de Máquina *Azure*, cliquei em "Criar um recurso";
## - Na barra de pesquisa, busquei por "Machine Learning" (aprendizado de máquina);
## - Selecionei "Azure Machine Learning" e em "Criar";
## - Após isso, segui conforme a documentação oficial me mostra, com o exemplo de aluguel de bicicletas:
### Configurações básicas:

#### Nome do trabalho: mslearn-bike-automl
#### Novo nome do experimento: mslearn-bike-rental
#### Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas
#### Tags: nenhuma
### Tipo de tarefa & data:

#### Selecionar tipo de tarefa: Regressão
#### Selecionar conjunto de dados: crie um novo conjunto de dados com as seguintes configurações:
#### Tipo de dados:
#### Nome: bike-rentals
#### Descrição: Dados históricos de aluguer de bicicletas
#### Tipo: Tabular
#### Fonte de dados:
#### Selecionar de arquivos da Web
#### URL da Web:
#### URL da Web: https://aka.ms/bike-rentals
#### Ignorar validação de dados: não selecione
#### Configurações:
#### Formato de arquivo: Delimitado
#### Delimitador: Vírgula
#### Codificação: UTF-8
#### Cabeçalhos de coluna: Somente o primeiro arquivo tem cabeçalhos
#### Pular linhas: Nenhum
#### O conjunto de dados contém dados de várias linhas: não selecione
#### Esquema:
#### Incluir todas as colunas diferentes de Caminho
#### Revisar os tipos detectados automaticamente
#### Selecione Criar. Depois que o conjunto de dados for criado, selecione o conjunto de dados de aluguel de bicicletas para continuar a enviar o trabalho de ML automatizado.

### Configurações da tarefa:

#### Tipo de tarefa: Regressão
#### Conjunto de dados: aluguel de bicicletas
#### Coluna de destino: Aluguéis (inteiro)
#### Definições de configuração adicionais:
#### Métrica primária: Erro quadrático médio da raiz normalizada
#### Explicar melhor modelo: Não selecionado
#### Use todos os modelos suportados: Nãoselecionado. Você restringirá o trabalho para tentar apenas alguns algoritmos específicos.
#### Modelos permitidos: selecione apenas RandomForest e LightGBM — normalmente você gostaria de tentar o maior número possível, mas cada modelo adicionado aumenta o tempo necessário para executar o trabalho.
#### Limites: expanda esta seção
#### Máximo de tentativas: 3
#### Máximo de tentativas simultâneas: 3
#### Nós máximos: 3
#### Limiar de pontuação métrica: 0,085 (de modo que, se um modelo atingir uma pontuação métrica quadrática média normalizada de 0,085 ou menos, o trabalho termina.)
#### Tempo limite: 15
#### Tempo limite de iteração: 15
#### Habilitar rescisão antecipada: Selecionado
#### Validação e teste:
#### Tipo de validação: Divisão de validação de trem
#### Porcentagem de dados de validação: 10
#### Conjunto de dados de teste: Nenhum
### Computação:

#### Selecione o tipo de computação: Serverless
#### Tipo de máquina virtual: CPU
#### Camada de máquina virtual: Dedicado
#### Tamanho da máquina virtual: Standard_DS3_V2*
#### Número de instâncias: 1

# Depois de enviado o trabalho, aguardei o serviço ser finalizado.
## Após o status estar como "Completo", segui a orientação clicando em "Visão geral" e, abaixo do "Nome do algorítmo" cliquei no hiperlink nomeado como "VotingEnsemble";
## Esse primeiro tópico foi para conferir as métricas e dados listados.

# Erros
## Assim como a tutora havia dito, recebi um erro  de dados não íntegros, então resolvi aguardar alguns minutos;
## Depois de aguardar, pude realizar o teste conforme a documentação pede, com êxito:
### Implantar e testar o modelo
#### Na guia Modelo para obter o melhor modelo treinado pelo seu trabalho de aprendizado de máquina automatizado, selecione Implantar e usar a opção Serviço Web para implantar o modelo com as seguintes configurações:
#### Nome: predict-rentals
#### Descrição: Prever aluguéis de ciclos
#### Tipo de computação: Instância de Contêiner do Azure
#### Habilitar autenticação: Selecionado
#### Aguarde o início da implantação - isso pode levar alguns segundos. O status de implantação para o ponto de extremidade de aluguel de previsão será indicado na parte principal da página como Em execução.
#### Aguarde até que o status Implantar seja alterado para Bem-sucedido. Isso pode levar de 5 a 10 minutos.

# Teste
## Após o tempo determinado, consegui realizar o teste com êxito nos pontos de extremidade e consegui o seguinte resultado:
### 🛑 422.6091407760338 🛑, semelhante à documentação oficial.

# Segue abaixo uma screenshot do trabalho realizado por ML
![image](https://github.com/Huguinhu/AI900/assets/144286137/93ddb7e5-adb8-4d67-b0c5-eb7960fac648)

