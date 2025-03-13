# Computação e Rede no Azure ☁

## Computação no Azure
A Computação no Azure é um serviço sob demanda que fornece recursos como discos, processadores, memória, rede e sistemas operacionais. Seus principais serviços incluem:
  - Máquinas Virtuais (VMs): oferecem um ambiente IaaS, permitindo a execução de sistemas operacionais e aplicativos personalizados.
    
  - App Services: plataforma gerenciada para hospedagem de aplicativos web, APIs e funções, sem necessidade de gerenciar infraestrutura.
    
  - Azure Kubernetes Service (AKS): serviço gerenciado para orquestração de contêineres Kubernetes, facilitando a implantação e o gerenciamento de aplicações em contêineres.
    
  - Área de Trabalho Virtual do Azure: solução de virtualização para desktops e aplicativos remotos, permitindo acesso seguro e gerenciado a partir da nuvem.

### Máquinas Virtuais no Azure
As Máquinas Virtuais do Azure (VMs) são servidores baseados em nuvem que oferecem suporte a ambientes Linux ou Windows. Elas são uma solução útil para migrações de lift-and-shift para a nuvem, permitindo a continuidade dos serviços sem grandes modificações na arquitetura.

#### Recursos e Benefícios:

  - Pacote do sistema operacional completo: Inclui o sistema operacional do host, proporcionando maior controle sobre a infraestrutura.
    
  - Flexibilidade: permite escolher e configurar diferentes tamanhos e tipos de VM conforme a necessidade.
    
  - Conjuntos de Dimensionamento: possibilitam a escalabilidade automática e o balanceamento de carga para ajustar os recursos de acordo com a demanda.
    
  - Alta Disponibilidade: ao utilizar Conjuntos de Disponibilidade, é possível distribuir VMs em diferentes domínios de falha, reduzindo riscos de indisponibilidade caso um rack apresente falhas. O ideal é ter pelo menos três domínios de falha para garantir redundância.
    
  - Domínios de Atualização: permitem gerenciar atualizações das máquinas virtuais sem impactar a operação contínua, sendo essa responsabilidade do cliente dentro do modelo IaaS.
    
  - Criação rápida com padrões predefinidos: O Azure permite criar máquinas virtuais a partir de imagens pré-configuradas, garantindo um ambiente padronizado e reduzindo o tempo de provisionamento.

### Área de Trabalho Virtual do Azure

A Área de Trabalho Virtual do Azure é um serviço de virtualização de desktops que permite a execução de aplicativos completos na nuvem. Ele cria um ambiente de virtualização sem necessidade de configurar servidores de gateway, proporcionando maior simplicidade na implantação.

#### Principais benefícios:

  - Ambiente personalizado: É possível configurar e personalizar a área de trabalho, instalando aplicativos, configurando o Microsoft 365 e adaptando completamente o ambiente às necessidades do usuário.
    
  - Ambiente mais seguro: Possui travas de segurança e maior rastreabilidade, tornando-se uma solução ideal para usuários remotos.
    
  - Múltiplos usuários simultâneos: Permite que vários usuários façam login ao mesmo tempo no mesmo computador, cada um com uma sessão isolada e recursos dedicados, otimizando a gestão dos recursos disponíveis.

### Serviços de Contêineres no Azure

Os Serviços de Contêineres do Azure oferecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional, respondendo automaticamente às mudanças de demanda. Eles são projetados para escalabilidade e eficiência, sendo compatíveis com Docker e outras tecnologias de contêineres.

#### Principais serviços:
  
  - Instâncias de Contêiner do Azure: uma oferta PaaS que executa um contêiner ou pod de contêineres no Azure. São mais rápidas e simples, pois não necessitam de uma máquina virtual para rodar.
  
  - Aplicativos de Contêiner do Azure: também uma oferta PaaS, mas com mais funcionalidades, como balanceamento de carga e escalabilidade automática, permitindo maior flexibilidade e facilidade no gerenciamento dos contêineres.
  
#### Contêineres e Microsserviços
  
  - Adequação para microsserviços: Contêineres são projetados para arquiteturas baseadas em microsserviços, pois são leves e altamente escaláveis.
  
  - Empacotamento de aplicativos e serviços: Aplicativos e serviços são empacotados em um contêiner que roda sobre o sistema operacional do host.
  
  - Execução simultânea: Vários contêineres podem rodar em um único sistema operacional do host, aproveitando melhor os recursos disponíveis.

### Azure Kubernetes Service (AKS)
O AKS é um serviço gerenciado de Kubernetes, que atua como uma solução de orquestração de contêineres para arquiteturas distribuídas e grandes volumes de contêineres.

#### Benefícios do AKS:

  - Gerenciamento automatizado: facilita a administração dos ciclos de vida dos contêineres.
    
  - Otimização de recursos: libera automaticamente contêineres que já concluíram suas tarefas, melhorando a eficiência e performance.
    
### Azure Functions: Computação sem Servidor.

O Azure Functions é uma oferta de Plataforma como Serviço (PaaS) baseada em eventos, que permite a execução de código de forma serverless (sem servidor dedicado). As funções são ativadas quando chamadas, sem necessidade de manter uma infraestrutura ativa durante períodos de inatividade.

#### Principais características:

  - Execução baseada em eventos: o código é acionado por eventos específicos.
  
  - Escalabilidade automática: aumenta ou reduz os recursos com base na demanda.
  
  - Eficiência e rapidez: ideal para cenários que exigem respostas rápidas e eficientes.
 
### Serviços de Aplicativos do Azure
Os Serviços de Aplicativos do Azure oferecem uma plataforma totalmente gerenciada para criação, implantação e escalabilidade de aplicativos web e APIs de forma rápida e eficiente. Essa solução é compatível com Windows e Linux, sendo uma excelente opção para hospedagem de aplicativos.

#### Principais características:
  
  - Hospedagem gerenciada: elimina a necessidade de gerenciar infraestrutura, permitindo que os desenvolvedores foquem na criação e otimização dos aplicativos.
  
  - Transições simplificadas: possibilita manter a versão em produção ao mesmo tempo em que outras versões estão em desenvolvimento, permitindo trocar facilmente qual versão da aplicação está ativa, facilitando testes e implantações contínuas.
  
  - Compatibilidade com várias linguagens: suporta desenvolvimento em .NET, .NET Core, Node.js, Java, Python e PHP.
  
  - Modelo PaaS: sendo uma Plataforma como Serviço, oferece alta segurança e conformidade, garantindo um ambiente confiável para aplicativos críticos.

###  Rede Virtual do Azure (VNET)
A Rede Virtual do Azure (VNET) permite a comunicação entre recursos dentro do Azure, conectando VNETs e suas sub-redes. No entanto, duas VNETs não se comunicam por padrão, sendo necessário um emparelhamento de rede para isso. Esse emparelhamento melhora a segurança, reduzindo o impacto de ataques laterais.

#### Principais estratégias de comunicação dentro da VNET:

  - Pontos de extremidade públicos: acessíveis pela internet.
  
  - Pontos de extremidade privados: restritos à rede interna.
  
  - Emparelhamento de rede: conecta redes privadas diretamente.
 
  - Sub-redes virtuais: segmentam a rede conforme necessário.

Além disso, endereços IP duplicados não podem existir entre redes que se comunicam, pois isso pode gerar conflitos.

### Conectividade entre Redes

  - Gateway de VPN: envia tráfego criptografado entre uma rede virtual do Azure e uma rede local através da internet pública, garantindo segurança.
  
  - ExpressRoute: oferece comunicação direta via um link dedicado (cabo físico), sem passar pela internet pública. Essa opção é mais cara e pode não ser viável em todos os casos, mas quando faz sentido geograficamente, melhora significativamente a performance e segurança.

### Segurança e Gerenciamento de DNS no Azure

A segurança de DNS no Azure é baseada no Gerenciador de Recursos, que permite controle baseado em funções, monitoramento e registro de logs. O serviço se destaca por sua confiabilidade e desempenho, aproveitando uma rede global de servidores DNS utilizando a tecnologia Anycast.

#### Principais recursos do DNS no Azure:

  - Gerenciamento unificado: facilita o controle de recursos internos e externos com um único serviço DNS.
  
  - Redes virtuais personalizáveis: permitem o uso de nomes de domínios privados e personalizados dentro de redes virtuais privadas.
  
  - Registros de alias: possibilitam apontar diretamente para um recurso do Azure.




