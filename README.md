# POC_Backend

POC desenvolvida para a palestra **Segurança e Qualidade podem andar juntas?** ministrada no evento **TDC Connections 2021**. Os slides usados na palestra estão disponíveis [aqui](https://github.com/larissafabiao/POC_Backend/blob/master/palestra%20TDC%20Connections.pdf).

Neste projeto estamos utilizando o **Ruby 2.7.2** e os seguintes pacotes:
```
gem "cucumber"
gem "httparty"
gem "pry"
gem "rspec"
gem "report_builder"
gem 'json'
gem 'aws-sdk-secretsmanager', '~> 1.44'
```

Estrutura do projeto:
```
./
│  ├── features/
│  │   ├── contracts/
│  │   ├── hooks/
│  │   ├── services/
│  │   │   ├── login/
│  │   │   │   ├──login_service.rb
│  │   ├── specifications/
│  │   │   ├── login/
│  │   │   │   ├──login.feature
│  │   ├── step_definitions/
│  │   │   ├── login/
│  │   │   │   ├──login_steps.rb
│  │   └── support/
│  │       ├── config/
│  │       │   └── environments.yml
│  │       ├── helpers/
│  │       │   ├── secret_manager.rb
│  │       │   ├── resource.rb
│  │       ├── env.rb
│  │       └── report_builder.rb
│  ├── reports/
│  └── cucumber.yml
├─ .gitignore
├─ Gemfile
├─ Gemfile.lock
└─ README.md
```


## Configurando ambiente local

Assumimos que você já ***possui o Ruby disponível no terminal***. Agora você precisará baixar as dependências utilizadas no projeto.

Para instalar o bundler executando o seguinte comando no terminal:
```
gem install bundler
```
Para baixar as dependências de pacote deste projeto abra a pasta do projeto no terminal e execute o comando:
```
bundler install
```

## Executando testes localmente

Para executar os testes localmente deste projeto no terminal e execute o comando:
```
cucumber -p @ambiente
```
Ou para um cenário específico:
```
cucumber -p @ambiente -t @myTag
```
