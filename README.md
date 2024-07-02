# Notas Arquitetura Limpa

### Pontos principais:
#### Escalabilidade 
- A abordagem para alcançar a escalabilidade pode variar mas geralmente envolve o design de componentes independentes e a distribuição eficiente de tarefas 
#### Modularidade
- A modularidade é essencial para a manuntenibilidade e extensibilidade de um sistema. 
- Dividir e conquistar (ao dividir um software coeso fica muito mais facil de se entender)
- Módulos bem definidos facilitam a reutilização de um código. 
##### Manutenbilidade:
 - refere-se à facilidade com que um sistema pode ser mantido e aprimorado ao longo do tempo. 
 - um boa arquitetura não compreende apenas a implementação inicial mas também as mudanças futuras. 
#### A arquitetura de software não é apenas a estrutura física de um sistema, mas a base que determina sua robustez e capacidade de adaptação. 

### Padrão arquitetural que visa criar sistemas de software altamente testáveis, flexíveis e escaláveis. A ideia central é separar as preocupações de neócios e de infra, mantendo uma separação clara e bem definida entre as camadas da aplicação. 

# BoilerPlate e Scaffolding
### Práticas essenciais que aceleram o processo de inicialização dos projetos, fornecendo uma base sólida e estrutura inicial economizando tempo e esforço 

### BoilerPlate 
- refere-se a trechos de código que são frequentemente repetidos.
- ajuda a evitar redundância 
- acelera implementação 
##### Vantagens:
- Produtividade
- Consistência
- Manutenção 
### Scaffolding
- refere-se a estrutura inicial do projeto.
- inclui organização de pastas, arquivos de configuração e ate mesmo implementações inicial de funcionamento. 
- estrutura solida na qual os devs possam construir sem começar do zero. 
##### Vantagens: 
- Padronização 
- Rapidez na inicialização
- Boas praticas. 
# 1. Clean Architecture.

Clean Arquitetura é um padrão de arquitetura de software que promove a separação de preocupações e a criação de sistemas altamente testáveis, flexíveis e independentes de detalhes de implementação (OBRIGAO ABSTRACAO)
#### Compreensão da arquitetura limpa
conceito arquitetural que estabelece diretrizes para organizar o código de um sistema de forma a isolar as preocupações e manter a flexibilidade. 
##### A ideia central é criar uma separação clara entre camadas do sistema. 

### Camadas 

#### Entidades: 
- Representam os conceitos de negocio do sistema.
- Encapsulam a logica de negocio e são independentes de qualquer detalhe de implementação. 
#### Use Cases: 
- Casos de uso representam as diferentes ações e operações que podem ser realizadas no sistemas. 
- Orquestram a interação entre as entidades e as outras chamados do sistema para realizar uma funcionalidade especifica 
- encapsulam a logica do negocio
- independentes de quaisquer implementação 
- Responsaveis por receber as entradas da interface do usuario
- retornar o resultado
#### Interface O/I:
- Sao responsaveis por interagir com as camadas externas do sismte (ex.: database e interface de usuario)
- Atuam como adaptadores entre essas camadas e os casos de uso
- Podem incluir controllers, presetations, gateways, db e etc...


# 1.2 Princípios de Clean Architecture
#### Independencia de framework
Deve ser independente de framework externo (posso trocar de DB quando quiser), frameworks de interface do usuário ou libs especificas de um determinado OS.
#### Testabilidade: 
O sistema deve ser projetado de forma a permitir testes automatizados em diferentes níveis. Isso é alcançado por meio da separação clara das regras de negócios das dependências externas. 
#### Separação de preocupações:
A arquitetura deve separar claramente as diferentes responsabilidades e preocupações do sistema. separa logica de negocio da camada de interface de usuário, bancos de dados e outras camadas externas.
Facilita na manutenção e evolução do sistema. 
#### Independência de UI:
Deve ser independente de UI, tendo camadas tão bem definidas que seja possível trocar de UI sem muitas alterações. 
#### Independência de DB:
Deve ser independente de DB, tendo camadas tão bem definidas que seja possível trocar de DB sem muitas alterações. 
#### Dependências direcionadas:
As dependências devem ser direcionadas de dentro pra fora, ou seja, as camadas internas não devem depender dos detalhes de implementação de camadas externas. 
