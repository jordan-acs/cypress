# Atividade ponderada sobre cypress - Jordan Andrade

## O que é o Cypress e para que serve?

O Cypress é uma ferramenta de automação de testes de software de código aberto projetada para testar aplicativos da web modernos. Ele se destaca por ser específico para testes end-to-end (E2E), ou seja, ele simula as interações do usuário com a aplicação da mesma forma que um usuário real faria. Isso inclui navegação entre páginas, preenchimento de formulários, cliques em botões, entre outras ações.

O Cypress é frequentemente utilizado para verificar se uma aplicação web funciona corretamente do início ao fim, garantindo que todas as partes estejam integradas de maneira adequada. Além dos testes E2E, o Cypress também pode ser usado para testes de unidade e integração, tornando-o uma ferramenta versátil para diferentes tipos de testes.

## Vantagens e desvantagens do Cypress em relação a outras ferramentas de teste

### Vantagens:

* Tempo de execução rápido: O Cypress possui um tempo de execução notavelmente rápido devido à sua arquitetura única, que executa diretamente no navegador.
* Arquitetura amigável: A estrutura de arquivos e a simplicidade na escrita de testes facilitam a adoção e manutenção do código.
* Integração contínua: Sua capacidade de integração fácil com pipelines de CI/CD torna o Cypress uma escolha popular em ambientes de desenvolvimento ágil.
* Facilidade de debug: A capacidade de visualizar a execução em tempo real e pausar o teste para inspeção facilita a identificação e resolução de problemas.

### Desvantagens:

* Compatibilidade de navegadores: O Cypress é otimizado para navegadores baseados no Chromium, o que pode limitar sua eficácia em ambientes que requerem testes em navegadores diferentes.
* Foco em aplicações web modernas: Pode não ser a escolha ideal para testar aplicações legadas ou aquelas que dependem fortemente de tecnologias específicas.

## Arquitetura do Cypress

A arquitetura do Cypress é baseada em um modelo cliente-servidor, onde o "Cypress Runner" atua como o cliente interagindo diretamente com o navegador em execução. Esse modelo oferece várias vantagens, como a capacidade de controlar a aplicação de forma mais direta e observar a execução em tempo real. O Cypress Runner executa comandos Cypress, como visitar uma URL, interagir com elementos da página e realizar assertivas para verificar o comportamento esperado.

## Seletores de elementos no Cypress

O Cypress suporta uma variedade de seletores para localizar elementos na página, incluindo seletores jQuery-like como cy.get('#elementId'), seletores específicos como cy.contains('texto') e cy.find('.classe'). Além disso, ele permite o uso de seletores CSS e XPath para oferecer flexibilidade na identificação de elementos, contribuindo para uma abordagem mais robusta na escrita de testes.

## Comandos e asserções no Cypress:

Os comandos Cypress são fundamentais para interagir com a aplicação durante os testes. Exemplos incluem :
* cy.visit(url):
  * Este comando navega para a URL especificada.
  * Exemplo: cy.visit('https://www.exemplo.com')
 
* cy.get(selector):
  * Utilizado para selecionar elementos na página, semelhante ao $ no jQuery.
  * Exemplo: cy.get('#botaoSubmit') seleciona o elemento com o id "botaoSubmit".

*cy.click([options]):
  * Simula um clique em um elemento selecionado.
  * Exemplo: cy.get('#botaoSubmit').click() aciona um clique no botão com id "botaoSubmit".

*cy.type(text, [options]):
  * Simula a digitação de texto em um campo de entrada.
  * Exemplo: cy.get('#campoNome').type('John Doe') preenche o campo com id "campoNome" com o texto 'John Doe'.

### Assertivas Cypress (should()):
As assertivas são usadas para verificar o estado esperado dos elementos após as interações. Aqui estão alguns exemplos comumente usados:

* should('exist'):
  * Verifica se o elemento existe na página.
    
* should('not.exist'):
  * Verifica se o elemento não existe na página.

* should('be.visible'):
  * Verifica se o elemento é visível.
    
* should('not.be.visible'):
  * Verifica se o elemento não é visível.

* should('have.value', expectedValue):
  * Verifica se o valor do elemento é igual ao expectedValue.

* should('contain', expectedText):
  * Verifica se o texto do elemento contém o expectedText.

* should('have.class', className):
  *Verifica se o elemento tem a classe CSS especificada.


## Descrição das etapas de preparação de um teste de interface, execução e verificação no Cypress:

### Preparação:

* Iniciar o Cypress usando npx cypress open, o que abre o Cypress Runner.
* Escrever testes em arquivos dentro do diretório "cypress/integration".
* Utilizar comandos Cypress para interagir com a aplicação, como cy.visit() para acessar URLs.

### Execução:

* Rodar os testes usando o Cypress Runner ou a linha de comando (npx cypress run).
* Acompanhar a execução no navegador enquanto os testes são realizados.

### Verificação:

* Analisar os resultados exibidos no Cypress Runner para verificar se os testes passaram ou falharam.
* Examinar mensagens de erro e logs para depurar problemas potenciais.

## Como estruturar testes de forma eficiente no Cypress?

* Organizar testes em pastas lógicas dentro de "cypress/integration" para facilitar a manutenção.
* Utilizar "fixtures" para dados de teste, separando os dados da lógica de teste.
* Criar comandos customizados para reutilização de lógica comum em vários testes.
* Usar os ganchos (before e beforeEach) para configurar o estado inicial do teste.
* Adotar boas práticas de nomeação para testes e arquivos, facilitando a identificação do propósito de cada teste.
* Dividir testes em casos de teste individuais, promovendo a reusabilidade e manutenção simplificada




