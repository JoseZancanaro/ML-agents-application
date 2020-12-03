https://github.com/Unity-Technologies/ml-agents/blob/release_10_docs/docs/Learning-Environment-Create-New.md#training-the-environment
versão: 10

# Criação do projeto e agente
- Adicionar o package ML-Agents ao projeto
- Criação do ambiente: chão, agente e alvo
- Implementar script do agente
- Configurações finais no Editor Unity

# Testar e treinamento
- Testar o ambiente manualmente, implementando a função Heuristic, marcar como heuristic only, depois colocar para default
- Treinar o ambiente
- Criar uma pasta /config na raíz do projeto
- Criar um arquivo de configuração .yaml em /config
- Instalar o pytorch - conda install -c pytorch pytorch
- Instalar pip3 install mlagents na raíz do projeto
- Rodar o treinamento: mlagents-learn <local do arquivo, /config/...> --run-id=<id>
- Possívelmente, visualizar os resultados instalando conda install -c conda-forge tensorboard
- tensorboard --logdir results, acessar localhost:6006
- tags axiliares --resume ou --force
- opcional - paralelizar o ambiente de treino, criando prefabs

# Usar o modelo treinado
- Criar uma pasta chamada TFModels, com o arquivo em .\results\<nome>\<nome.onnx>
- Selecionar o prefab ir na janela de inspeção do agente
- Em behavior parameters, selecionar o modelo treinado (.onnx)