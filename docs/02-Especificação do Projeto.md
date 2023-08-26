## Especificações do Projeto

<span style="color:red">Pré-requisitos: <a href="https://github.com/ICEI-PUC-Minas-PMV-ADS/AutoApp/blob/6e8341aac6887998ec783beca8ce97995d7e896a/docs/01-Documenta%C3%A7%C3%A3o%20de%20Contexto.md"> Documentação de Contexto</a></span>


Nesta seção, apresentamos o diagrama de personas, histórias de usuários, requisitos funcionais e não funcionais, além das restrições identificadas para o desenvolvimento deste projeto.

## Personas

As personas levantadas durante o processo de entendimento do problema são apresentadas na Tabela que se seguem.

| Cod | Tipo do Usuário               | Descrição                                                                                                                                                                                     |
| --- | ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Usuário Leigo                 | Uma pessoa não técnico que possui um iPhone, mas tem dificuldades em lidar com problemas técnicos. Ele busca uma solução fácil para receber ajuda quando seu dispositivo apresenta problemas. |
| 2   | Técnico com Certificado Apple | Um profissional que deseja usar a plataforma para acessar manuais de reparo e obter informações técnicas detalhadas sobre produtos Apple, para melhor atender seus clientes.                  |
| 3   | Estudante Universitário       | Um estudante que possui um MacBook e depende muito dele para suas tarefas acadêmicas. Ele relata que procura uma maneira rápida de obter assistência em caso de falhas.                       |
| 4   | Cliente Fiel Apple            | Um entusiasta da Apple com vários produtos da marca, busca uma plataforma unificada para gerenciar seus dispositivos e receber suporte quando necessário.                                     |
| 5   | Usuário Empresarial           | Uma pequena empresa que utiliza dispositivos Apple em sua operação diária, ele precisa de um canal eficiente para agendar reparos e minimizar a interrupção nas atividades comerciais.

## Histórias de Usuários

A partir da compreensão do dia a dia das personas identificadas para o projeto, foram registradas as seguintes histórias de usuários.

| EU COMO... `PERSONA`      | QUERO/PRECISO ... `FUNCIONALIDADE`                               | PARA ... `MOTIVO/VALOR`                                                    |
| ------------------------- | ---------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Usuário Leigo             | relatar problemas com meu iPhone                                 | receber instruções simples e obter assistência técnica de maneira fácil.   |
| Técnico Certificado Apple | acessar manuais de reparo detalhados para produtos Apple         | executar reparos com mais eficácia e precisão.                             |
| Estudante Universitário   | agendar reparos rápidos para o meu MacBook                       | evitar interrupções em minhas atividades acadêmicas e continuar produtivo. |
| Cliente Fiel Apple        | receber notificações sobre o status do reparo do meu dispositivo | ficar atualizado sobre o progresso e estimativas de conclusão.             |
| Usuário Empresarial       | um canal eficiente para agendar reparos                          | minimizar a interrupção nas atividades comerciais                          |

## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto. Para determinar a prioridade de requisitos, aplicamos uma técnica de priorização de requisitos e detalhamos, em sequência, como a técnica foi aplicada.

A técnica MoSCoW foi aplicada para priorização dos requsitos:

- Must Have (Tenho que fazer)
- Should Have (Devo fazer)
- Could Have (Poderia fazer)
- Won’t Have (Não vou fazer)

Nesse sentido a ordem de importância das tarefas vai seguindo uma ordem decrescente, em que "Must Have" são as tarefas mais relevantes e as "Won’t Have" são tarefas que podem ficar para depois.

### Requisitos Funcionais

|ID    | Descrição do Requisito  | Prioridade |
|------|-----------------------------------------|----|
| RF-001 | O sistema deverá permitir a criação de um perfil de usuário para o responsável do aparelho Apple ao seu e-mail.	ALTA 
| RF-002 | OO sistema deverá permitir a alteração e a exclusão dos dados de usuários, nesse caso, excluindo também qualquer aparelho Apple  vinculado a ele.	ALTA
| RF-003 | O sistema deverá permitir a inserção, a alteração e a exclusão dos dados de prestadores de serviços afiliados.	ALTA 
| RF-004 | O sistema deverá permitir a adição de equipamento ( modelo,tipo do equipamento, etc.), permitindo a exibição de seus dados básicos.	ALTA
| RF-005 |O sistema deverá armazenar os dados  de manutenções efetuadas.	ALTA
| RF-006 | O sistema deverá gerar relatórios sobre os dados preenchidos pelos usuários. | MÉDIA |
| RF-007 |O sistema deverá permitir a edição e a exclusão dos dados do aparelho Apple. | MÉDIA |
| RF-008 | O sistema deve emitir lembretes para os usuários. | MÉDIA |
| RF-009 | O sistema deverá permitir a busca em lojas conveniadas próximas a sua localidade.	BAIXA

### Requisitos não Funcionais

|ID     | Descrição do Requisito  |Prioridade |
|-------|-------------------------|----|
| RNF-001 | O sistema deve ser responsivo para rodar em diversos dispositivos móveis | ALTA | 
| RNF-002 | O sistema deve ser implementado utilizando React Native. | ALTA |
| RNF-003 | A persistência dos dados será feita no banco MySQL.  |  MÉDIA |
| RNF-004 | O sistema deve processar requisições do usuário em no máximo 11 segundos. |  BAIXA |

## Restrições

1. **Objetivo Alvo**: Desenvolver uma aplicação móvel para dispositivos iOS (iPhone e iPad) que ofereça um canal de assistência de manutenção e reparo de produtos da Apple.

2. **Funcionalidades principais**:

   | Cod | Funcionalidade                             | Descrição                                                                                                                                                                           |
   | --- | ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | 1   | Cadastro de usuários e produtos Apple.     | Permitir que os usuários se cadastrem na plataforma usando informações básicas, como nome, e-mail e senha.                                                                          |
   | 2   | Solicitação de assistência técnica.        | Oferecer um formulário de solicitação de assistência técnica, onde os usuários podem descrever brevemente o problema que estão enfrentando com seu dispositivo Apple.               |
   | 3   | Acompanhamento do status de reparo.        | Após a solicitação, os usuários podem verificar o status do reparo através de uma página de acompanhamento simples.                                                                 |
   | 4   | Notificações sobre atualizações no status. | Enviar notificações por e-mail ou mensagem SMS quando houver uma atualização significativa no status do reparo.                                                                     |
   | 5   | Acesso a guias de solução de problemas.    | Disponibilizar algumas guias básicas de solução de problemas para problemas comuns que os usuários possam enfrentar, como reinicialização de dispositivo, problemas de conexão etc. |
   | 6   | Avaliação e feedback pós-reparo.           | Após o reparo ser concluído, permitir que os usuários forneçam feedback sobre a qualidade do serviço.                                                                               |

        |        
## Especificações em Matriz de rastreabilidade

| Necessidade/Requisito            | Funcionalidade/Atividade                         | Evidência                               |
| -------------------------------- | ------------------------------------------------ | --------------------------------------- |
| Acompanhamento de reparos        | Desenvolvimento do aplicativo móvel              | Aplicativo móvel em funcionamento       |
| Comunicação clara sobre status   | Implementar atualizações de status em tempo real | Status atualizado visível no aplicativo |
| Redução de ligações/mensagens    | Integrar notificações de status por push         | Notificações enviadas e recebidas       |
| Cadastro de usuários             | Criar sistema de registro e login                | Cadastro e login funcionais             |
| Informar tipo de reparo e prazo  | Mostrar detalhes do serviço e prazo de conclusão | Informações corretas exibidas           |
| Indicação de conclusão de reparo | Atualização do status para "Concluído"           | Mudança de status visível               |
| Melhorar reputação da empresa    | Coletar avaliações dos clientes                  | Avaliações positivas recebidas          |
| Fidelização do cliente           | Implementar programas de fidelidade              | Benefícios para usuários fiéis          |


## Gestão de Orçamento

| Orçamento                     |     (R$)         |
| ----------------------------- | ------------ |
| **Recursos Humanos**            | **150,000** |
|   - Gerente de Projeto (4 meses)  | 12,000  |
|   - Desenvolvedor (6 meses) x 5   | 138,000 |
| **Hardware**                    | **15,000**  |
|   - Computadores e Equipamentos   | 10,000  |
|   - Dispositivos Móveis           | 5,000   |
| **Rede**                        |  **5,000**   |
|   - Equipamentos de Rede          | 3,000   |
|   - Instalação e Configuração     | 2,000   |
|  **Software**                    | **10,000**  |
|   - Licenças de Software          | 8,000   |
|   - Ferramentas de Desenvolvimento | 2,000  |
|  **Serviços**                     | **8,000**  |
|   - Consultoria Externa           | 5,000   |
|   - Suporte Técnico               | 3,000   |
| **Total**                       | **196,000** |

Detalhes para cada item:

- Recursos Humanos:
   - Gerente de Projeto (4 meses): O Gerente de Projeto receberá R$ 12,000 pelo período de 4 meses.
   - Desenvolvedores (6 meses) x 5: Cada um dos 5 desenvolvedores receberá R$ 23,000 (totalizando R$ 115,000) pelo período de 6 meses.

- Hardware:
   - Computadores e Equipamentos: O custo de hardware é de R$ 10,000 para adquirir computadores e outros equipamentos necessários.
   - Dispositivos Móveis: R$ 5,000 para dispositivos móveis necessários para o desenvolvimento e teste.

- Rede:
   - Equipamentos de Rede: Os equipamentos de rede têm um custo de R$ 3,000.
   - Instalação e Configuração: A instalação e configuração da rede têm um custo de R$ 2,000.

- Software:
   - Licenças de Software: R$ 8,000 para adquirir as licenças de software necessárias para o desenvolvimento.
   - Ferramentas de Desenvolvimento: R$ 2,000 para adquirir ferramentas específicas de desenvolvimento.

- Serviços:
   - Consultoria Externa: Custa R$ 5,000 para contratar serviços de consultoria externa.
   - Suporte Técnico: R$ 3,000 para serviços de suporte técnico ao longo do projeto.
