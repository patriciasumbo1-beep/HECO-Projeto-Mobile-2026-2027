# H-ECO

## Reporte cidadão do estado de contentores de lixo

## Proposta de projeto

### Nome do projeto

**H-ECO** — uma aplicação móvel para reporte do estado de enchimento de contentores de lixo, com notificação direta às autoridades municipais responsáveis pela recolha de resíduos.

## Enquadramento do projeto

### 2.1 Ideia e descrição

O H-ECO é uma aplicação móvel que permite a qualquer cidadão reportar, em tempo real, o estado de enchimento de um contentor de lixo. Os estados disponíveis são:

- Médio;
- Cheio.

O reporte é efetuado através da introdução do código do contentor ou da leitura do código QR afixado no mesmo.

O envio do reporte exige uma fotografia do contentor e a captura automática da localização do utilizador. Estes mecanismos destinam-se a reduzir a ocorrência de reportes falsos ou efetuados a partir de locais afastados do contentor.

O utilizador também pode consultar a aplicação para localizar contentores próximos onde possa depositar os seus resíduos.

Os operadores municipais de recolha recebem notificações automáticas sempre que um contentor da sua zona é marcado como cheio. Após efetuarem a recolha, registam o contentor como recolhido através de uma fotografia tirada diretamente na aplicação. O estado do contentor é então reposto para vazio, ficando novamente disponível para novos reportes.

### 2.2 Pesquisa sobre o contexto

Entre janeiro e meados de setembro de 2025, o Portal da Queixa registou 266 reclamações relacionadas com higiene urbana em Portugal, representando um aumento de 10 % face ao ano anterior. Os concelhos de Lisboa, Almada e Sintra lideraram o número de ocorrências, com queixas sobretudo relacionadas com lixo acumulado nas ruas, contentores cheios e falta de recolha atempada.

### 2.3 Objetivos

- Reduzir o tempo médio entre o momento em que um contentor fica cheio e a sua recolha efetiva;
- Aumentar a eficiência das equipas de recolha, direcionando-as apenas para contentores efetivamente cheios;
- Criar um canal de participação cívica simples e de baixo esforço para o cidadão comum;
- Gerar um histórico de dados que permita estimar a taxa de enchimento de cada contentor e prever quando voltará a ficar cheio;
- Reduzir a incidência de lixo acumulado fora dos contentores, situação frequentemente motivada pela sua lotação;
- Permitir que o cidadão procure um contentor com espaço disponível antes de sair de casa.

## Público-alvo

### Cidadão participante

Morador ou qualquer pessoa com idade e literacia digital suficientes para utilizar a aplicação, com motivação cívica ou preocupação com a limpeza urbana. Interage com a aplicação de forma pontual e rápida.

### Operador de recolha municipal

Trabalhador de campo das equipas de higiene urbana que utiliza a aplicação em contexto operacional, privilegiando a rapidez e a clareza em detrimento da componente estética.

## 2.5 Pesquisa sobre outras aplicações existentes

### Sensoneo — Eslováquia

A aplicação cidadã da Sensoneo informa sobre o contentor vazio mais próximo, o tipo de resíduo e o nível de enchimento. No entanto, os dados são obtidos através de sensores ultrassónicos instalados fisicamente em cada contentor. Trata-se, por isso, de um sistema apenas de leitura, sem possibilidade de reporte pelos cidadãos.

### Contentores inteligentes da LIPOR — Portugal

Este projeto-piloto está implementado nos concelhos de Gondomar, Póvoa de Varzim, Valongo e Vila do Conde. Registou mais de 10 000 aberturas até ao final de abril. O sistema centra-se na separação de resíduos recicláveis através de sensores instalados nos contentores, não no reporte do seu estado pelos utilizadores.

### Na Minha Rua — Câmara Municipal de Lisboa

O portal municipal permite reportar genericamente problemas urbanos, incluindo situações relacionadas com higiene urbana. No entanto, é um canal mais lento e genérico, sem leitura de códigos QR, verificação através de fotografia ou localização e notificação direta às equipas de recolha.

| Solução            | Requer sensores físicos | Permite reportes de cidadãos | Verificação antifraude | Notificação direta ao operador |
| :----------------- | :---------------------: | :--------------------------: | :--------------------: | :----------------------------: |
| Sensoneo           |           Sim           |             Não              |     Não aplicável      |              Sim               |
| LIPOR              |           Sim           |             Não              |     Não aplicável      |              Sim               |
| Na Minha Rua — CML |           Não           |             Sim              |          Não           |              Não               |
| H-ECO              |           Não           |             Sim              |          Sim           |              Sim               |

O H-ECO posiciona-se entre estas abordagens: não exige um investimento em sensores instalados em cada contentor, mas oferece um fluxo dedicado, rápido e verificado. Desta forma, combina a fiabilidade de um sistema de monitorização com um custo de implementação reduzido.

## 3.1 Guião — Cidadão reporta o estado de um contentor

1. O cidadão abre a aplicação H-ECO.
2. Introduz o código do contentor ou lê o código QR afixado no mesmo.
3. A aplicação recolhe automaticamente a localização do utilizador e confirma a sua proximidade ao contentor.
4. O utilizador tira uma fotografia do contentor.
5. Seleciona o estado observado:
   - Médio;
   - Cheio.
6. Confirma o envio do reporte.
7. Caso o estado reportado seja «cheio», o sistema notifica automaticamente os operadores responsáveis pela zona.

## 3.2 Guião — Operador marca um contentor como recolhido

1. O operador recebe uma notificação relativa a um contentor cheio.
2. Abre a aplicação e consulta a lista ou o mapa de contentores filtrados pelo estado «cheio».
3. Desloca-se até ao contentor indicado e procede à recolha.
4. Tira uma fotografia do contentor após a recolha.
5. Marca o contentor como recolhido na aplicação.
6. O sistema regista a recolha e repõe o estado do contentor para «vazio».
7. O contentor fica novamente disponível para novos reportes.

## 3.3 Guião — Cidadão consulta o mapa antes de depositar resíduos

1. O cidadão pretende depositar resíduos e abre a aplicação H-ECO.
2. Consulta imediatamente o mapa de contentores, sem necessidade de efetuar qualquer leitura de código.
3. Visualiza os contentores próximos, identificados por cores de acordo com o seu estado:
   - Verde — vazio ou com espaço disponível;
   - Amarelo — estado médio;
   - Vermelho — cheio.
4. Escolhe o contentor com mais espaço disponível.
5. Desloca-se até ao contentor selecionado.

## Plano de trabalhos

O trabalho será desenvolvido ao longo de 14 semanas, seguindo uma metodologia ágil, com entregas nas semanas 4, 9 e 14, de acordo com os marcos definidos no briefing do projeto.

Nas semanas 1 e 2 será realizada a análise e a conceptualização do projeto, incluindo a definição da ideia, a pesquisa de mercado, a identificação dos casos de utilização e a especificação dos requisitos.

Nas semanas 3 e 4, o trabalho avançará para a criação dos protótipos iniciais, através de wireframes no Figma, para a modelação preliminar da base de dados e para a consolidação da presente proposta.

Entre as semanas 5 e 9, o trabalho será centrado na implementação do back-end, da API REST e da base de dados MySQL, bem como no início do desenvolvimento da aplicação Android. Esta fase culminará num protótipo funcional correspondente à segunda entrega.

Entre as semanas 10 e 14 será realizada a integração completa entre a aplicação, o back-end e a base de dados. Serão também implementados o método numérico de estimativa da taxa de enchimento dos contentores, os testes de usabilidade e a documentação final para a terceira entrega.

## 5. Projeto charter e WBS

### 5.1 Projeto charter — Síntese

| Campo           | Descrição                                                                                             |
| :-------------- | :---------------------------------------------------------------------------------------------------- |
| Nome do projeto | H-ECO                                                                                                 |
| Objetivo        | Reduzir o tempo entre o enchimento dos contentores e a sua recolha, através do reporte pelos cidadãos |
| Contexto        | Projeto de aplicação móvel — Licenciatura em Engenharia Informática, IADE                             |
| Estudante       | Humaira                                                                                               |

### 5.2 Estrutura analítica do projeto — WBS

| Fase               | Principais tarefas                                                                                  |
| :----------------- | :-------------------------------------------------------------------------------------------------- |
| Análise e conceção | Definição de requisitos, casos de utilização, modelo de domínio e pesquisa de mercado               |
| Planeamento        | Plano de trabalhos, calendarização e configuração do repositório no GitHub                          |
| Prototipagem       | Criação de wireframes e protótipos no Figma                                                         |
| Implementação      | Desenvolvimento da aplicação Android, da API REST, da base de dados e integração do método numérico |
| Testes             | Realização de testes de usabilidade                                                                 |
| Apresentação       | Preparação e realização da apresentação final                                                       |

## 6. Requisitos

### 6.1 Requisitos funcionais

| Código | Descrição                                                                                     |
| :----- | :-------------------------------------------------------------------------------------------- |
| RF01   | O sistema deve permitir criar uma conta e efetuar a autenticação do utilizador.               |
| RF02   | O utilizador deve poder pesquisar contentores próximos e disponíveis para depositar resíduos. |
| RF03   | O utilizador deve poder reportar o estado de um contentor.                                    |
| RF04   | O utilizador deve poder consultar o histórico dos seus próprios reportes.                     |
| RF05   | O operador deve poder visualizar os contentores organizados por estado.                       |
| RF06   | O operador deve poder marcar um contentor como recolhido.                                     |
| RF07   | O sistema deve notificar os operadores quando um contentor estiver cheio.                     |
| RF08   | O sistema deve estimar a previsão de enchimento com base no histórico de reportes.            |

### 6.2 Requisitos não funcionais

| Categoria       | Requisito                                                                                                                         |
| :-------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| Usabilidade     | O fluxo de reporte — leitura do código, fotografia, seleção do estado e envio — deve poder ser concluído em menos de 30 segundos. |
| Privacidade     | As fotografias e os dados de localização devem ser tratados como dados pessoais.                                                  |
| Disponibilidade | A aplicação deve funcionar com conectividade instável e estar disponível 24 horas por dia, 7 dias por semana.                     |
| Desempenho      | A notificação ao operador deve ser enviada em menos de 1 minuto após o reporte.                                                   |
| Escalabilidade  | A solução deve estar preparada para suportar vários municípios sem necessidade de uma reformulação estrutural.                    |
| Segurança       | O sistema deve incluir mecanismos de prevenção de reportes falsos.                                                                |
