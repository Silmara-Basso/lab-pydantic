# lab-pydantic
Teste de versionamento de modelo e Pydantic para validação de dados

# Construindo e Operacionalizando Pipeline de Previsão em Tempo Real

### O Pydantic é uma biblioteca Python que facilita a criação de modelos de dados de forma eficiente e segura. Ele utiliza type hints para validação e serialização automática dos dados, garantindo que os valores fornecidos correspondam aos tipos esperados. Além disso, permite transformar dados entre diferentes formatos e gerar mensagens de erro detalhadas.

# Instruções

1- Abra um terminal ou prompt de comando, navegue até a pasta com os arquivos e execute o comando abaixo para criar a imagem Docker:
```
docker compose build --no-cache
```

2- No mesmo terminal ou prompt de comando, execute o comando abaixo para treinar o modelo e salvar os metadados:
```
docker compose run --rm app python -m app.treino
```

3- Agora abra OUTRO terminal ou prompt de comando, navegue até a pasta com os arquivos e execute o comando abaixo para iniciar o container da API:
```
docker compose up --build
```

4- Agora abra outro terminal ou prompt de comando, navegue até a pasta com os arquivos e execute o comando abaixo para consumir a API:
```
python cliente.py 
```
Execute de forma alternada os itens 2 e 4
A cada execução do 2 uma nova versão do modelo é treinada e salva, e como estamos lendo do disco o modelo toda vez que chamamos o cliente, ele sempre usa a versão mais recente.



