Desafio AWS CloudFormation — Implementando minha Primeira Stack

Sobre o Projeto

Este repositório faz parte do meu aprendizado na formação AWS Cloud Practitioner / Cloud DevOps da DIO, onde realizei o desafio “Implementando sua Primeira Stack com AWS CloudFormation”.

O objetivo foi automatizar a criação de recursos na nuvem AWS utilizando o AWS CloudFormation, aplicando os conceitos de Infrastructure as Code (IaC) — ou seja, infraestrutura tratada como código, o que permite padronização, versionamento e reutilização de ambientes com segurança e eficiência.

Durante o desafio, eu compreendi como transformar processos manuais em automação total, garantindo que toda a estrutura de recursos (como S3, EC2, RDS, Lambda etc.) possa ser criada com apenas um arquivo YAML.

 O que é o AWS CloudFormation?

O AWS CloudFormation é um serviço da Amazon Web Services que permite modelar, criar e gerenciar infraestrutura na nuvem de forma automatizada.

Em vez de criar manualmente cada recurso no console, eu posso descrever toda a arquitetura em um template (arquivo .yaml ou .json), e o CloudFormation executa esse modelo para criar uma Stack com todos os recursos definidos.

Esses templates podem ser reutilizados quantas vezes for necessário, e eu só pago pelos recursos criados, não pelo uso do serviço em si.
Além disso, posso versionar o template no GitHub, atualizar stacks com segurança e replicar o mesmo ambiente em outras regiões ou contas AWS.

Durante o desafio, aprendi os seguintes conceitos e práticas fundamentais:

Fundamentos:

O que é uma Stack e como ela representa um conjunto de recursos AWS gerenciados como uma unidade.

Como criar e configurar templates YAML/JSON no formato exigido pelo CloudFormation.

Como acompanhar o ciclo de vida da Stack (CREATE_IN_PROGRESS, CREATE_COMPLETE, ROLLBACK_COMPLETE).

Automação e Estrutura:

A estrutura principal de um template (AWSTemplateFormatVersion, Description, Resources).

A diferença entre criar manualmente e automatizar via código.

Como definir propriedades como AccessControl, DeletionPolicy e LifecycleConfiguration.

Aplicação de Infrastructure as Code (IaC) para reduzir erros e garantir consistência.

Segurança e Boas Práticas:

Aplicação de criptografia de dados com o AWS KMS (Key Management Service).

Uso de Bucket Policies para exigir conexões seguras (HTTPS).

Geração de nomes dinâmicos de buckets com variáveis (!Sub ${AWS::StackName} e ${AWS::AccountId}).

Criação de recursos Serverless com o transformador AWS::Serverless-2016-10-31.

Durante o curso e o desafio, aprendi também sobre a importância das boas práticas em CloudFormation, abordadas nos talks e explicações dos instrutores da DIO:

Automatizar é padronizar: todo recurso deve nascer de um template versionado.

Evitar criação manual: o console é apenas para testes; produção deve ser via IaC.

Reutilizar templates: uma Stack bem construída pode ser aplicada em vários ambientes (dev, teste e produção).

Usar parâmetros e variáveis: tornam o template dinâmico e flexível.

Segurança é prioridade: criptografia e HTTPS não são opcionais — são boas práticas obrigatórias.

Esses pontos me ajudaram a entender que CloudFormation não é só uma ferramenta de criação, mas também um método de governança e segurança em infraestrutura.

Conclusão

Esse desafio foi essencial para consolidar meu entendimento sobre Infrastructure as Code (IaC) e o uso do AWS CloudFormation na prática.
Aprendi a modelar, automatizar e proteger recursos em nuvem de forma profissional.

Hoje entendo que CloudFormation não é apenas sobre “criar recursos”, mas sobre controlar, versionar e garantir conformidade na infraestrutura.

Essa foi minha primeira Stack completa e segura, criada 100% via código — um marco importante na minha jornada como desenvolvedora e futura especialista em cloud.
