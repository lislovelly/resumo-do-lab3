# resumo-do-lab3

## Configurando uma Instância de Banco de Dados na Azure
Configurar uma instância de banco de dados na Azure envolve uma série de etapas detalhadas e considerações para garantir que o sistema atenda às necessidades específicas da aplicação. Aqui está um resumo do que aprendi durante esse processo:

## Criação de Máquinas Virtuais
O primeiro passo na configuração de uma instância de banco de dados é a criação de uma máquina virtual (VM). Esse processo requer atenção a vários detalhes:

Sistema Operacional: A escolha do sistema operacional depende do tipo de banco de dados que será utilizado. Por exemplo, um banco de dados SQL Server normalmente rodará no Windows, enquanto um banco de dados MySQL pode ser configurado tanto em Windows quanto em Linux.

Imagem e Arquitetura: Ao selecionar a imagem e arquitetura da VM, é necessário especificar o tipo de imagem (por exemplo, Windows Server 2019, Ubuntu 20.04) e a arquitetura (x86, x64). A plataforma já mostra o tamanho da instância e o custo estimado mensalmente.

Responsabilidade: É importante lembrar que tudo o que for criado é de responsabilidade do usuário. Isso inclui a configuração, manutenção e segurança da máquina virtual.
Criar uma VM na Azure não é um processo simples. Existem várias opções e configurações que precisam ser definidas, e é essencial entender o que cada configuração exige para, posteriormente, implementar corretamente a estratégia no código.

## Configurando um Banco de Dados SQL
Para configurar um banco de dados SQL na Azure, são necessários vários passos detalhados:

Nome do Banco de Dados: Especificar um nome claro e identificável para o banco de dados.

Servidor: Se não houver um servidor existente, é preciso criar um novo servidor. Isso envolve definir um nome para o servidor, a região onde ele será hospedado e as credenciais de administrador.

Autenticação: Configurar a autenticação do banco de dados, definindo o administrador e as políticas de segurança.

Redundância do Armazenamento e SLA: Escolher a estratégia de redundância do armazenamento (LRS, ZRS, GRS, GZRS) e definir o SLA desejado, que já mostra a previsão do custo mensal.

Todo o cenário de gerenciamento está associado ao modelo de serviço escolhido. Quanto mais envolvimento você tiver na configuração e manutenção, menos a Microsoft estará envolvida, e vice-versa.

## Modelos de Serviço na Azure
Na Azure, existem diferentes modelos de serviço que determinam o nível de gerenciamento necessário:

Infraestrutura como Serviço (IaaS): Este modelo demanda mais do nosso lado, pois somos responsáveis pela gestão completa da máquina virtual, incluindo sistema operacional, rede, armazenamento e aplicativos.

Plataforma como Serviço (PaaS): Aqui, a Microsoft gerencia a infraestrutura subjacente, enquanto somos responsáveis pelo desenvolvimento e gestão dos aplicativos.

Software como Serviço (SaaS): Este é o modelo que dá menos dor de cabeça, pois a Microsoft gerencia tudo, incluindo o aplicativo. Nosso papel é simplesmente usar o software.
Estratégias de Replicação e Custos

## A escolha das estratégias de replicação e as regiões onde os dados serão armazenados também influenciam a SLA e os custos:

LRS (Locally Redundant Storage): Replica dados dentro de um único datacenter.

ZRS (Zone-Redundant Storage): Replica dados entre diferentes zonas de disponibilidade na mesma região.

GRS (Geo-Redundant Storage): Replica dados entre regiões geográficas, garantindo maior resiliência a desastres.

GZRS (Geo-Zone-Redundant Storage): Combina a replicação entre zonas e regiões para a máxima disponibilidade e resiliência.

Essas opções não apenas impactam a confiabilidade e disponibilidade dos dados, mas também afetam diretamente os custos mensais associados ao armazenamento e gerenciamento dos dados.
