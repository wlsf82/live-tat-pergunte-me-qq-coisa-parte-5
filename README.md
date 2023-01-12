# Live TAT - Pergunte-me qualquer coisa - Parte V

✅ --> Perguntas respondidas

❌ --> Perguntas que não soube ou não pude responder

## Perguntas e respostas

**Fonte principal das perguntas:** [https://shorturl.at/chUX1](https://shorturl.at/chUX1).

### Leonardo Costa

1. Hoje, qual a versão mais estável do cypress?
Atualmente possuo um projeto com a versão 9.7.0 do cypress, para fazer a atualização para a versão mais recente terei muito trabalho? Existe alguma recomendação para essa atualização? ✅

<details><summary>Resposta</summary>
</br>

Considero a versão @latest sempre como a mais estável. Para saber qual a última versão, recomendo consultar o [_Changelog_ do Cypress](https://docs.cypress.io/guides/references/changelog).

Além disso, recomendo assistir a _Live_ [Migração do projeto de boas práticas em automação de testes para a v12 do Cypress](https://youtu.be/7_k21pPsSq8), na qual demonstro como é simples fazer a atualização.

</details>
</br>

2. Como sabemos quando devemos automatizar os testes? ✅

<details><summary>Resposta</summary>
</br>

Sempre que percebermos que certo trabalho manual é repetitivo.

</details>
</br>

### Victor Schlindwein

Fala Walmyr, buenas meu caro.
Você consegue demonstrar algum exemplo de projeto grande que utiliza o cypress para testes e2e?
Pergunto isso mais no contexto de conseguir me basear em padrões de arquiteturas.
Algumas recomendação pra um projeto em arquitetura cycommands não virar um Page Objetcts CyCommands? ✅

<details><summary>Resposta</summary>
</br>

- [Cypress Real World App (RWA)](https://github.com/cypress-io/cypress-realworld-app)
- [Playlist explorando os testes de GUI, API, unidade e CI da RWA](https://youtube.com/playlist?list=PL-eblSNRj0QGU6gO4Yhb27ZwaCASG-lQl)
- [GitLab-Cypress](https://github.com/wlsf82/gitlab-cypress)

</details>
</br>

### Alisson Max do Amaral Fernandes

Fala, prof! Algum exemplo de utilização do cypress com CD/CI na prática? Algum exemplo de gerenciador de testes que integra com o Cypress? Abraço! ✅

<details><summary>Resposta</summary>
</br>

Mantenho o seguinte projeto, o qual exemplifica ambos CI, como CD: https://github.com/wlsf82/hackernews. Tal projeto também é integrado com o Cypress Cloud, para a gestão dos testes.

</details>
</br>

### Gustavo José da Silva

Achei bem bacana a integração contínua utilizando o GitHub Actions com o dashboard do Cypress. Apenas uma contribuição mesmo, as vezes seria uma pauta legal para demonstrar na live. ✅

<details><summary>Resposta</summary>
</br>

Já fiz duas _Lives_ sobre o Dashboard do Cypress, agora chamado de Cypress Cloud. Seguem os links:

- [Explorando o Dashboard do Cypress.io](https://youtu.be/kZhA8BgGPT0)
- [Gestão de testes flaky usando o Dashboard do Cypress](https://youtu.be/MO18galnqMY)

</details>
</br>

### Thiago Fragoso

1. Fala, Walmyr! Gostaria de indicações de sites para treinar automação com Cypress. Obrigado! ✅

<details><summary>Resposta</summary>
</br>

Além da [Cypress RWA](https://github.com/cypress-io/cypress-realworld-app), recomendo procurar por projetos _open-source_ que possuam imagens Docker. Dessa forma, é fácil montar um ambiente local para praticar.

Seguem alguns exemplos:

- [GitLab CE (versão do curso intermediário de Cypress da Escola TAT)](https://hub.docker.com/r/wlsf82/gitlab-ce)
- [GoCD Server](https://hub.docker.com/r/gocd/gocd-server/)
- [Mattermost Docker Preview Image](https://hub.docker.com/r/mattermost/platform)

Além disso, os [cursos da Escola TAT](https://www.udemy.com/user/walmyr/) disponibilizam aplicações para a prática de automação de testes, com aplicações web para buscas, CRUD, formulários HTML, etc.

</details>
</br>

2. Walmyr, gostaria de entender melhor sobre o cy.intercept e network requests. Embora eu tenha entendido como usar, ainda sinto falta de como funciona e a ligação entre eles. Se for um tema interessante pra live, agradeceria. ✅

<details><summary>Resposta</summary>
</br>

Recomendo a leitura do seguinte conteúdo, publicado em inglês no Dev Community: [`cy.request` vs. `cy.intercept`](https://dev.to/walmyrlimaesilv/cy-request-vs-cy-intercept-cmi).

</details>
</br>

### Wallace Dias

Boa Walmyr, você já realizou conexão do Cypress com banco de dados oracle ou outro? Teria alguma recomendação ou boa prática para implementar essa conexão na arquitetura do projeto? ✅

<details><summary>Resposta</summary>
</br>

Demonstrei um exemplo na _Live_ chamada [O problema da massa de dados em testes automatizados](https://youtu.be/ASCAt2tuG_A), onde neste caso, criei um mecanismo utilitário para acesso à um banco MongoDB, onde fazia uso da funcionalidade [`cy.exec()`](https://on.cypress.io/exec) para a execução npm scripts para o _drop_ e _seed_ do banco de dados.

Além disso, encontrei os seguintes _plugins_ na [página oficial de _Plugins_ do Cypress](https://docs.cypress.io/plugins):

- [cypress-firebase](https://github.com/prescottprue/cypress-firebase)
- [cypress-indexeddb](https://github.com/thisdot/open-source/tree/main/libs/cypress-indexeddb)
- [cypress-mongodb](https://github.com/Zaista/cypress-mongodb)

Além destes, encontrei este outros para integração com bancos de dados Oracle e MySQL, procurando direto no [site oficial do npm](https://www.npmjs.com/):

- [cypress-oracle-db](https://www.npmjs.com/package/cypress-oracle-db)
- [@cypress-tools/mysql](https://www.npmjs.com/package/@cypress-tools/mysql)

</details>
</br>

### David Alves Oliveira

Gostaria de saber como armazenar um texto de um elemento para usar depois. Tentei com aliás e outras sugestões mas sem sucesso. ✅

<details><summary>Resposta</summary>
</br>

Isso tem "cheiro" de má prática, visto que na maioria dos casos que precisamos disso estamos criando dependências entre os testes.

Falei sobre isso na _Live_ [Levando dados de um teste para outro com Cypress tasks](https://youtu.be/917kJtI2z_M).

No entanto, esses dias vi a [seguinte publicação no LinkedIn oficial do Cypress](https://www.linkedin.com/posts/cypress%2Eio_cypress-plugin-store-activity-7018257096211091456-FG27?utm_source=share&utm_medium=member_desktop), sobre o [cypress-plugin-store](https://www.npmjs.com/package/cypress-plugin-store). Quem sabe ajude.

</details>
</br>

### Maira Dias

Olá Walmyr, alguma recomendação sobre como executar testes automaticamente pela ferramenta Jenkins? ✅

<details><summary>Resposta</summary>
</br>

Minha recomendação, independente do serviço de integração contínua, é escrever testes independentes uns dos outros, o mais otimizados possíveis, rápidos e confiáveis.

Também recomendo a definição de npm scripts que possam ser usados na integração contínua (ex.: `npm test`, `npm run test:smoke`, `npm run test:mobile`, etc.)

Depois, é só chamar tais scrips em seu _pipeline_ de _CI_.

Para exemplos especício do Jenkins, recomendo [esta seção da documentação oficial do Cypress](https://docs.cypress.io/guides/continuous-integration/ci-provider-examples#Jenkins).

</details>
</br>

### Vinicius Ribeiro

Quais tipos de relatorio ou saída de resultados podem ser gerados no processo de CI? ✅

<details><summary>Resposta</summary>
</br>

- Logs do terminal
- Artefatos como _screenshots_, vídeos, relatórios XML e HTML

No entanto, não sou o maior fã de relatórios HTML e falo disso na _Live_ [Por que não uso relatórios cheios de fru-fru com Cypress?](https://youtu.be/m6FTTl5F3VU)

Por fim, para uma melhor gestão dos testes automatizados, é possível integrar os mesmos com o serviço do Cypress na nuvem, o [Cypress Cloud](https://cloud.cypress.io/).

</details>
</br>

### Wellington Costa

​Cypress pode ser usado mesmo sendo java no backend? ✅

<details><summary>Resposta</summary>
</br>

Sim, o Cypress pode testar qualquer tipo de aplicação web, independente da tecnologia usada para a "construção" da mesma.

</details>
</br>

### Guilherme de Sousa

Em um ambiente aonde tenho a massa de dados toda controlada (graças a Dios), estou com uma necessidade de aplicar cálculos de DESCONTOS e IMPOSTOS em determinados produtos e validar se a conta bate. Sei que o backend pode fazer isso nos testes unitários, mas como eu poderia fazer essas validações dos cálculos nos testes de API/UI? ✅

<details><summary>Resposta</summary>
</br>

Por qual motivo você duplicaria tal validação, a qual, como você mesmo disse, poderia ser testada à nível de unidade no backend?

</details>
</br>
