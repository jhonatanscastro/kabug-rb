# kabug-rb
Repositório do projeto Kabug com Cucumber, Capybara e Ruby

## Como executar o projeto

* Importante ter o Ruby instalado

### Instalar o bundler

`
gem install bundler
`

### Instalar as Gems (dependências do projeto)
`
bundle install
`

### Executar no modo CI gerando report em JSON

`
bundle exec cucumber -p ci
`

### Executar no modo local (minha maquina)

`
bundle exec cucumber
`