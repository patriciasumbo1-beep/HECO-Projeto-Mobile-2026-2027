# H-ECO: Reporte Cidadão do Estado de Contentores de Lixo

O **H-ECO** é um projeto académico de uma aplicação móvel destinada a melhorar a comunicação entre os cidadãos e as equipas municipais responsáveis pela recolha de resíduos urbanos.

A proposta centra-se no reporte do estado de enchimento dos contentores, através de um código QR ou do código identificador do contentor, com recurso a fotografia e localização GPS para reduzir reportes incorretos. Quando um contentor é identificado como cheio, o sistema deverá informar as equipas responsáveis pela recolha.

> **Estado de repositório:** neste momento, o repositório contém a documentação inicial e a estrutura de organização do projeto. Não foram encontrados código-fonte, ficheiros de configuração de uma aplicação, dependências ou instruções de execução de um protótipo no conteúdo actualmente disponível.

## Índice

- [Problema e contexto](#problema-e-contexto)
- [Objetivos](#objetivos)
- [Público-alvo](#público-alvo)
- [Funcionalidades previstas](#funcionalidades-previstas)
- [Fluxos principais](#fluxos-principais)
- [Requisitos funcionais](#requisitos-funcionais)
- [Requisitos não funcionais](#requisitos-não-funcionais)
- [Tecnologias e implementação](#tecnologias-e-implementação)
- [Organização do repositório](#organização-do-repositório)
- [Instalação e execução](#instalação-e-execução)
- [Configuração](#configuração)
- [Estado actual e limitações](#estado-actual-e-limitações)
- [Autores](#autores)

## Problema e contexto

A gestão de resíduos urbanos pode ser dificultada pela existência de contentores cheios, pela acumulação de lixo no espaço público e pela falta de informação atempada para as equipas de recolha.

A proposta do H-ECO refere que, entre janeiro e meados de setembro de 2025, o Portal da Queixa registou 266 reclamações relacionadas com higiene urbana em Portugal, correspondendo a um aumento de 10 % face ao ano anterior. As reclamações incidiam sobretudo em lixo acumulado, contentores cheios e recolhas efectuadas tardiamente.

O projecto procura responder a este problema através de um canal de comunicação mais directo, orientado para uma situação concreta: identificar o estado de um contentor e transmitir essa informação às equipas responsáveis.

## Objetivos

Com base na proposta disponível no repositório, os principais objectivos do H-ECO são:

- melhorar a comunicação entre os cidadãos e as equipas municipais de recolha;
- facilitar a identificação de contentores cheios;
- reduzir o tempo entre o enchimento de um contentor e a sua recolha;
- apoiar uma utilização mais eficiente das rotas e dos recursos das equipas de recolha;
- disponibilizar aos cidadãos informação sobre o estado e a localização dos contentores;
- reduzir a deposição de resíduos fora de contentores que já não tenham capacidade disponível;
- criar um histórico de reportes que possa apoiar a estimativa da taxa de enchimento e a previsão de futuros períodos de lotação.

Estes objectivos pertencem à proposta do projecto. A implementação técnica correspondente não pode ser confirmada no estado actual do repositório, uma vez que não foram encontrados ficheiros de código da aplicação.

## Público-alvo

### Cidadão que efectua o reporte

Qualquer residente ou pessoa que se encontre junto de um contentor e tenha literacia digital suficiente para utilizar a aplicação. A utilização prevista é pontual, rápida e orientada para comunicar um problema imediato.

### Operador de recolha municipal

Trabalhador de campo das equipas de higiene urbana que consulta os contentores sinalizados e regista a recolha. Neste contexto, a rapidez, a clareza da informação e o apoio à organização da rota são prioridades.

## Funcionalidades previstas

As funcionalidades abaixo fazem parte da proposta funcional do H-ECO. Não devem ser interpretadas como funcionalidades já confirmadas por código neste repositório.

- criação de conta e autenticação;
- identificação de contentores através de código QR ou código do contentor;
- reporte do estado de enchimento de um contentor;
- selecção de um estado observado, nomeadamente **médio** ou **cheio**;
- captura de uma fotografia do contentor no momento do reporte;
- recolha da localização GPS para confirmar a proximidade ao contentor;
- envio de notificações às equipas de recolha quando um contentor é marcado como cheio;
- mapa ou pesquisa de contentores próximos e disponíveis;
- consulta do histórico dos reportes efectuados pelo próprio utilizador;
- visualização de contentores organizados por estado para os operadores;
- registo da recolha pelo operador, incluindo uma fotografia do contentor vazio;
- reposição do estado do contentor para **vazio** após a recolha;
- estimativa da previsão de enchimento com base no histórico de reportes.

## Vantagem proposta

O H-ECO propõe um fluxo dedicado, rápido e verificado sem depender da instalação de sensores físicos em todos os contentores. A combinação de código identificador, fotografia e localização pretende reduzir reportes falsos, mantendo uma abordagem com menor dependência de equipamento instalado no terreno.

Esta é uma vantagem prevista no conceito do projecto e não um resultado medido ou validado através do código actualmente disponível.

## Fluxos principais

### Reporte de um contentor pelo cidadão

O fluxo descrito na proposta é o seguinte:

1. O cidadão abre a aplicação H-ECO.
2. Introduz o código do contentor ou lê o código QR afixado no mesmo.
3. A aplicação recolhe, quando disponível, a localização GPS e verifica a proximidade ao contentor.
4. O cidadão tira uma fotografia do contentor.
5. Selecciona o estado observado: **médio** ou **cheio**.
6. Confirma e envia o reporte.
7. Quando o estado indicado é **cheio**, o sistema deverá notificar os operadores responsáveis pela zona.

Não existe actualmente código no repositório que permita confirmar o comportamento concreto destes passos.

### Recolha pelo operador municipal

De acordo com a proposta, o fluxo do operador é composto pelas seguintes etapas:

1. O operador recebe uma notificação relativa a um contentor cheio.
2. Abre a aplicação e consulta o mapa ou a lista de contentores a recolher.
3. Desloca-se até ao contentor indicado.
4. Efectua a recolha, tira uma fotografia do contentor vazio e marca-o como recolhido na aplicação.
5. O sistema repõe o estado do contentor para **vazio**, tornando-o novamente disponível para futuros reportes.

Este fluxo está documentado como comportamento previsto. Não foi possível confirmá-lo através de uma implementação existente no repositório.

### Consulta de um contentor disponível

A proposta prevê que o cidadão possa abrir a aplicação e consultar um mapa com os contentores próximos, sem ter de iniciar um reporte ou efectuar uma leitura de código. Os contentores deverão ser apresentados de acordo com o seu estado, permitindo ao cidadão escolher uma localização com espaço disponível.

A proposta identifica as seguintes cores como exemplo de representação visual:

- verde — contentor vazio ou com espaço disponível;
- amarelo — contentor com estado médio;
- vermelho — contentor cheio.

Como não existe código ou protótipo funcional disponível no repositório, não é possível confirmar se este fluxo ou esta representação visual já estão implementados.

## Requisitos funcionais

A tabela seguinte reproduz os requisitos funcionais definidos para o projecto, assinalando que a sua implementação não pode ser verificada no estado actual do repositório.

| Código | Requisito                                                                 | Estado verificável no repositório                                               |
| :----- | :------------------------------------------------------------------------ | :------------------------------------------------------------------------------ |
| RF01   | O utilizador deve poder criar uma conta e iniciar sessão.                 | Não confirmado: não existe código de autenticação disponível.                   |
| RF02   | O utilizador deve poder pesquisar contentores próximos e disponíveis.     | Não confirmado: não existe implementação de mapa ou pesquisa disponível.        |
| RF03   | O utilizador deve poder reportar o estado de um contentor.                | Não confirmado: não existe código da aplicação disponível.                      |
| RF04   | O utilizador deve poder consultar o histórico dos seus próprios reportes. | Não confirmado: não existe código ou base de dados disponível.                  |
| RF05   | O operador deve poder visualizar contentores por estado.                  | Não confirmado: não existe interface ou serviço disponível.                     |
| RF06   | O operador deve poder marcar um contentor como recolhido.                 | Não confirmado: não existe implementação disponível.                            |
| RF07   | O sistema deve notificar os operadores quando um contentor estiver cheio. | Não confirmado: não existem serviços de notificação ou configuração disponível. |
| RF08   | O sistema deve estimar a previsão de enchimento com base no histórico.    | Não confirmado: não existe algoritmo ou implementação disponível.               |

## Requisitos não funcionais

A proposta apresenta os seguintes requisitos não funcionais:

- concluir o fluxo de reporte em menos de 30 segundos;
- tratar fotografias e dados de localização como dados pessoais;
- suportar conectividade instável e disponibilidade contínua;
- enviar a notificação ao operador em menos de 1 minuto após o reporte;
- suportar vários municípios sem uma reformulação estrutural;
- incluir mecanismos de prevenção de reportes falsos.

Nenhum destes requisitos pode ser declarado como implementado com base no conteúdo actualmente existente no repositório. Não foram encontrados código-fonte, testes, ficheiros de configuração, métricas ou documentação técnica que permitam verificar o seu cumprimento.

## Tecnologias e implementação

### Tecnologias confirmadas

A única tecnologia directamente confirmada no conteúdo actual do repositório é **Markdown**, utilizada no ficheiro `00_Identificacao/info.md`.

### Tecnologias previstas na proposta

A documentação do projecto menciona uma futura aplicação Android, uma API REST e uma base de dados MySQL. Contudo, não foram encontrados no repositório ficheiros de uma aplicação Android, uma API, um esquema de base de dados, dependências ou ficheiros de compilação que permitam confirmar a sua utilização.

Por esse motivo, não são indicados comandos de instalação, versões ou ferramentas específicas para essas tecnologias.

## Arquitectura e funcionamento geral

A arquitectura técnica ainda não pode ser determinada a partir do repositório. A proposta descreve, de forma conceptual, uma solução composta por:

1. uma aplicação móvel utilizada pelo cidadão e pelo operador;
2. um mecanismo de identificação do contentor através de código QR ou código próprio;
3. serviços de localização e captura de fotografia;
4. um sistema de gestão do estado dos contentores;
5. notificações destinadas às equipas municipais;
6. um histórico de reportes para consulta e previsão.

Esta descrição representa a arquitectura funcional prevista, não uma arquitectura técnica confirmada por código.

## Organização do repositório

A estrutura existente está organizada por áreas de documentação e materiais do projecto:

```text
.
├── 00_Identificacao/
│   └── info.md
├── 01_Memoria_Descritiva/
│
├── 02_Imagens/
│
├── 03_Videos/
│
├── 04_Documentacao_Tecnica/
│
├── 05_Artefactos/
│
├── 06_Dados_Investigacao/
│
└── 07_Autorizacoes/

```

### Descrição das pastas

| Pasta                     | Conteúdo actualmente disponível                                                                     |
| :------------------------ | :-------------------------------------------------------------------------------------------------- |
| `00_Identificacao`        | Documento `info.md` com a proposta do projecto, os objectivos, os fluxos previstos e os requisitos. |
| `01_Memoria_Descritiva`   | Pasta reservada para a memória descritiva.                                                          |
| `02_Imagens`              | Pasta reservada para imagens.                                                                       |
| `03_Videos`               | Pasta reservada para vídeos.                                                                        |
| `04_Documentacao_Tecnica` | Pasta reservada para documentação técnica.                                                          |
| `05_Artefactos`           | Pasta reservada para artefactos do projecto.                                                        |
| `06_Dados_Investigacao`   | Pasta reservada para dados de investigação.                                                         |
| `07_Autorizacoes`         | Pasta reservada para autorizações.                                                                  |

## Instalação e execução

Não existem actualmente no repositório código-fonte, um projecto compilável, dependências ou scripts de execução. Assim, não é possível fornecer comandos de instalação ou execução que possam ser confirmados como funcionais.

Para consultar a documentação existente, basta abrir o ficheiro [`00_Identificacao/info.md`](00_Identificacao/info.md) no GitHub ou num editor de texto compatível com Markdown.

## Configuração

Não foi encontrada configuração técnica que necessite de ser aplicada. O repositório não contém, entre outros elementos, ficheiros de ambiente, credenciais, chaves de API, ficheiros de dependências, configuração de base de dados ou configuração de serviços externos.

## Estado actual e limitações

### Estado actual

O repositório encontra-se numa fase inicial de organização documental. Inclui:

- a proposta de projecto em `00_Identificacao/info.md`;
- pastas preparadas para documentação, imagens, vídeos, artefactos, dados de investigação e autorizações.

### Limitações conhecidas

Com base na análise do conteúdo disponível:

- não existe código-fonte da aplicação móvel;
- não existe API REST ou outro serviço de back-end;
- não existe base de dados ou esquema de dados;
- não existem dependências ou ficheiros de compilação;
- não existem testes automatizados ou testes de usabilidade no repositório;
- não existem imagens, vídeos ou protótipos funcionais guardados nas pastas respectivas;
- não é possível confirmar quais dos requisitos funcionais e não funcionais já foram implementados;
- não é possível executar o projecto a partir do conteúdo actual.

A proposta menciona um plano de trabalho de 14 semanas, mas o repositório não contém informação adicional que permita confirmar o cumprimento de tarefas semanais ou de marcos de desenvolvimento.

## Autores

- Humaira Farage Bemat (20250997)
- Margarida Patrícia Sumbo (20252385)
- Tiago João Hora Inácio (20252137)

## Contexto académico

Projecto de aplicação móvel no âmbito da **Licenciatura em Engenharia Informática — IADE**.
