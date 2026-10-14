# Estante: contexto para o Claude Code

## Objetivo
App Android de lista de leitura (Estante), em Kotlin e Jetpack Compose.
É um projeto educativo para o Arthur aprender arquitetura Android e Compose,
e também um projeto de portfólio.

## Modo de trabalho (obrigatório)
- Ensine antes de codificar: explique o conceito e depois o passo.
- Não escreva o código inteiro. Dê dicas, revise o que eu escrevi e aponte erros.
- Se eu pedir código, explique cada parte: o que faz, por que e como replicar.
- Uma fase por vez. Só avance para a próxima quando eu confirmar.
- Se não tiver certeza de uma API ou versão, diga isso e aponte a documentação oficial.

## Escopo
- Requisitos: docs/Requirements.md. A v1 é RF01 a RF08 e RNF01 a RNF03.
- A v2 (RF09 a RF12) fica fora do escopo por enquanto.
- Decisões de arquitetura: docs/adr/.
- Wireframes: docs/wireframe-*.png.

## Arquitetura
- MVVM com fluxo unidirecional: o estado desce e os eventos sobem.
- ViewModel expõe um UiState único via StateFlow.
- Repository é a única fonte de dados. Room para o banco local, Retrofit para a API.
- Hilt para injeção de dependência.
- Pastas por funcionalidade: ui/list, ui/add, ui/detail, data/local, data/remote, di, model.

## Stack
- Kotlin, Jetpack Compose com Material 3.
- Navigation Compose com rotas tipadas.
- Room, Hilt, Retrofit com kotlinx.serialization.
- JUnit e Turbine para testes.
- Versões de bibliotecas no libs.versions.toml. Não invente versões.

## Convenções
- Commits no padrão feat:, fix:, docs:, test:, chore:. Um commit por passo que funciona.
- Composables reutilizáveis recebem `modifier: Modifier = Modifier`.
- Telas com ViewModel ficam separadas da parte sem ViewModel (ex.: ListScreen e ListScreenContent).
- Ícones clicáveis têm contentDescription (acessibilidade, RNF03).
- Textos da interface vão para strings.xml. O idioma ainda está em definição.

## Estado atual
- Fase em andamento: 1 (composables e Preview).
- Veja os commits recentes para o progresso.