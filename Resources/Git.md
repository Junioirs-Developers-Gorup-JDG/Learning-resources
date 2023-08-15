## Banches

- Main 
	- Travada
	- Merge apenas quando for fazer deploy de uma nova versão
- Develop
	Usada para unir as features, com o objetivo de testar a integração entre features
- Branch com nome de Feature
	Usada para desenvolver, atualizar, remover uma feature.

Exemplo: 

Supondo o desenvolvimento de um site com tela de login e dashboard. Teriamos o esquema de branches [assim](https://www.figma.com/file/EacWUSe7dVVknmfhp5lVya/Untitled?type=whiteboard&node-id=0%3A1&t=7oKZFGHvWBucZCDT-1)

## Commit Patterns

Titulo - Tipo: descrição breve

Descrição - Necessária apenas em commits complexos;

### Tipos de commit

- `feat` - Indica que seu commit inclui um **novo recurso**/**funcionalidade**.
	Exmplos: 
		- Desenvolvimento de um novo contexto(Front-End);
		- Desenvolvimento de um novo modelo(Back-End);
- `fix` - Indica que seu commit está **solucionando um problema**;
- `docs` - Indica que houveram **mudanças na documentação**(Não inclui alterações em código).
	Exemplo: Criação do readme do seu repositório;
- `test` - Indica **alterações em testes**, criação, alteração ou exclusão de testes unitários;
- `build` - Indica modificações em **arquivos de build**.
- `perf` - Indica alterações de código que estejam relacionadas a **performance**.
- `style` - Indica alteração na **formatações de código**, semicolons, trailing spaces, lint... (Não inclui alterações em código).
- `refactor` - Indica mudanças devido a **refatorações que não alterem sua funcionalidade**.
	Exemplo: Uma alteração no formato como é processada determinada parte da tela, mas que manteve a mesma funcionalidade, ou melhorias de performance devido a uma revisão;
- `chore` - Indica atualizações de tarefas de build, configurações de administrador, pacotes.
	Exemplo: Quando é instalado um novo pacote no seu projeto e o package.json é atualizado;

## Materiais para estudo

- [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)
- [Fluxo de trabalho de Gitflow](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow)
