# Angular
Projeto Angular para a Disciplina Linguagem de Script
<img src="https://angular.io/assets/images/logos/angular/angular.png">

Foi implementada uma Single Page Aplication (SPA) utilizando o framework Angular. O projeto é baseado nos cursos on-line sobre Angular feitos nos sites loiane.training e <a href=
"https://www.udemy.com/curso-de-desenvolvimento-web-com-es6-typescript-e-angular-4/learn/v4/overview">Curso Udemy</a>, entre dezembro de 2017 e fevereiro de 2018.
<img src="http://helderrangel.com.br/imgens/blocos-angular.png>
Desenvolvido localmente, sendo o Windows 10, Nodejs 8.9.3 e NPM 5.6.0, Angular Cli 1.6.5 e o editor de scripts Visual Studio Code, com TypeScript 2.5.3. Foram utilizados o frameworks Bootstrap 4.0, bem como bibliotecas JavaScript como Jquery 3.3 e Hammer 2.0.8. O Angular tem como requisito recomendável a versão node 6.9.x ou  superior e npm 3.x.x ou superior. Para identificar as respectivas versões instaladas no sistema operacional basta usar os comandos node -v e npm -v, no terminal. 

Ao utilizar algumas extensões do VSCode sua produtividade pode aumentar, automatizando a importação de módulos nativos do Angular, por exemplo. A sugestão é de instalar extensões como a de Balram Chavan - chamada de "Angular 2,4 and upcoming latest Typescript Snippets". Outra exensão útil é de John Papa, "Angular v2 TypeScript Snippets". "Auto Import", de steiates, importa automaticamente módulos do Angular, o único problema é que ele mistura os módulos importados do desenvolver com os do Angular. Os módulos do Angular devem ser listados no topo, logo abaixo, separados por uma linha, devem seguir listados os módulos do desenvolvedor. A extensão HTML snippets facilita o trabalho com HTML, já o "vscode-icons", de Roberto Huertas, identifica cada um dos tipos de arquivos usados nos projetos.

O Nodejs pode ser baixado a partir do site https://nodejs.org.

A instalação de requisitos podem ser feitas via NPM:

npm install -g typescript

npm install -g @angular/cli





Para o curso de Loiane Groner você vai precisar instalar Bootstrap, Materialize, Hammer e JQuery. Logo a seguir sugiro que você faça algo diferente para outros projetos que envolvam Bootstrap, mas para o curso de Loiane.training execute os seguintes comandos no terminal de seu sistema opercional:

npm install materialize-css --save
npm instalar angular2-materialize --save

O app.module.ts deve deve receber os seguintes códigos, seguindo recomendações do https://angular.io/guide/styleguide

import 'materialize-css';
import { MaterializeModule } from 'angular2-materialize';

Já o arquivo de configuração do angular/cli deve receber na propriedade script:
[
"../node_modules/jquery/dist/jquery.js",
  "../node_modules/hammerjs/hammer.js",
  "../node_modules/materialize-css/dist/js/materialize.js"
  ]
Um detalhe importante, para você que vai usar o Bootstrap dentro de um projeto Angular, siga as instruções do site https://ng-bootstrap.github.io/#/getting-started. De acordo com a documentação você vai instalar o ng-bootstrap, seguindo os passos a seguir:

1) Depois de instalar o Angular e o Bootstrap (CSS)

npm install --save @ng-bootstrap/ng-bootstrap

2)Depois de instalado, importe o módulo principal

import {NgbModule} from '@ng-bootstrap/ng-bootstrap'

Outros módulos e aplicações que precisem do Bootstrap podem fazer a importação do Ngbmodule:

3) Agora, liste o módulo importado no seu módulo raiz e quaisquer módulos de aplicativos adicionais que façam uso dos componentes nesta biblioteca. O método exato será um pouco diferente para o módulo raiz, terminando com o código NgbModule.forRoot():

import {NgbModule} from '@ng-bootstrap/ng-bootstrap'

@NgModule({
  declarations: [AppComponent, ...],
  imports: [NgbModule.forRoot(), ...],
  bootstrap: [AppComponent]
})
export class AppModule {
}
Ler a documentação pode tornar seu trabalho mais produtivo. Conheça melhor os recursos do Angular/cli no site https://github.com/angular/angular-cli/wiki/stories.

Para criar o projeto, use o comando ng g new nomedoprojeto - que deve começar com uma letra. Em seguida, entre no diretório nomedoprojeto para criar ali componentes, diretivas, serviços, utilizando o Angular cli:

- para criar módulo: ng g m nomedomodulo
- para criar componente: ng g c nomedocomponente
- para criar serviço: ng g s nomedoservico
- para criar diretiva: ng g d nomedadiretiva ????

Foi utilizado o json-server com uma API Rest fake para interpretar requisições http e respondê-las. Para isso, instale o recurso:
npm install json-server
No caso, para rodar a funcionalidade deve-se executar o comando a seguir no mesmo local onde está o arquivo json.
json-server --watch banco-de-dados.json

<a><strong>Principais recursos do Angular</a></strong>
- Two-way Data binding
- Injeção de Dependências
- Criação de diretivas
- Modularização e reuso (Controllers, Services e Filters)
- Testabilidade


Two-way Data binding: É um recurso mágico do mesmo que permite a atualização em realtime que é feito através do objeto [()], chamada de caixa de banana, qualquer interação na view será refletida no modelo e assim sucessivamente

Injeção de dependência: Sua função é de separar responsabilidades através da aplicação service , para que a função fique
bem definida , de fácil manutenção e testáveis.

Criação de diretivas: Permite criar diversas indicações como ele próprio é uma extensão do html por exemplo

Modularização e reuso: Usando controllers , Services e Filters é possível transformar o resultado de uma expressão,
aplicando algum tipo de formatação ou restrição de dados.
Exemplo: validação de formulários de compra, checando se foram informados um número mínimo de caracteres.

Ler a documentação pode tornar seu trabalho mais produtivo. Conheça melhor os recursos do Angular/cli no site https://github.com/angular/angular-cli/wiki/stories.
