## Edian Firewall

O Endian Firewall é uma [distribuição Linux](https://pt.wikipedia.org/wiki/Distribui%C3%A7%C3%A3o_Linux) especializada em roteamento/firewall que possui uma interface unificada de gerenciamento. Foi desenvolvido pela italiana [Endian Srl](https://pt.wikipedia.org/w/index.php?title=Societ%C3%A0_a_Responsabilit%C3%A0_Limita&action=edit&redlink=1) e pela comunidade.

O Endian Firewall foi originalmente baseado no [IPCop](https://pt.wikipedia.org/wiki/IPCop), sendo que este é um fork do projeto [Smoothwall](http://en.wikipedia.org/wiki/SmoothWall).
[Wikipédia](https://pt.wikipedia.org/wiki/Endian_Firewall).

![Image](/images/logo.jpg)

- A Versão 3.0 contém os seguintes pacotes e funcionalidades:
- Firewall (ambas direções)
- Gateway
- VPN com OpenVPN ou IPsec
- Web Antivírus
- Web Anti-spam
- E-Mail Antivírus
- E-Mail Anti-spam
- Transparente HTTP-Proxy
- Filtro de Conteúdo
- Ponto de Acesso sem Fio Seguro
- Protocolo de Inicialização de Sessão - SIP e Suporte para VoIP
- Tradução de Endereços de Rede NAT
- Multi endereços IP (apelidos/aliases)
- HTTPS web interface
- Estatísticas de Conexão
- Log de tráfego na rede
- Redirecionamento de logs para servidor externo
- DHCP-Servidor
- Servidor de Tempo NTP-Servidor
- Sistema de Detecção de Intrusos IDS
- Sistema de Prevenção de Intrusos IPS
- ADSL-Modem Suporte

### Redes do Endian Firewall

O Endian separa as redes conectadas a ele em quatro zonas principais (Red, Green, Blue and Orage), as duas zonas mais importantes - VERDE e VERMELHA.
![Image](/images/zones.png)


- **VERMELHA**: esta é chamada de segmento não confiável, ou seja, a WAN: Abrange todas as redes fora do Endian, em termos gerais, a Internet, e é a fonte de conexões de entrada. Possibilita configuração do modo failover.

- **VERDE**: a rede interna, ou seja, a LAN. Esta zona é a mais protegida e é dedicado às estações de trabalho e nunca deve ser acessado diretamente a partir da zona vermelha. É também a única zona que, por padrão pode acessar a interface de gerenciamento.

- **LARANJA** ou **DMZ**: esta zona deve hospedar os servidores que precisam acessar a Internet para fornecer serviços (por exemplo, SMTP / POP, SVN e HTTP). Se um invasor consegue quebrar um dos serviços/servidores, o mesmo ficará preso dentro da DMZ e não será capaz atingir a zona verde.

- **AZUL**: zona Wi-Fi, ou seja, a zona que deve ser usado por clientes sem fio para acessar a Internet. As redes sem fio, muitas vezes não são seguras, então a ideia é isolar todos os clientes conectados sem fio em sua própria zona sem acesso a qualquer outra zona, exceto RED.

### Instalando Endian Firewall

**1** Inicie  o computador com opção de BOOT via CD-ROM, será apresentado a tela ISOLINUX,
pressione ENTER para continuar com instalação.

![Image](/images/install1.jpg)

**2** Selecione a linguagem English, após a escolha pressione TAB para descer ate o botão OK em seguida aperte a tecla ENTER. Será apresentada tela de boas vindas e
perguntara se deseja realizar a instalação do Endian pressione ENTER.

![image](/images/install2.jpg)

**3** Proximo passo informa que todos os arquivos do seu disco serão apagados, prossiga com selecionando YES e depois pressione OK para continuar. Em seguida será perguntado
se deseja habilitar porta serial do computador, escolha opção NO em seguida OK.

![Image](/images/install3.jpg)

**4** Finalizado processo de instalação devemos configurar endereço IP/MÁSCARA da rede VERDE. Este IP será utilizado como Gateway padrão e para acesso ao Endian via SSH e
interface WEB, após configurar IP escolha opção OK.

![Image](/images/ip.jpg)

**5** Por fim, surge aviso indicando que você ejete o CD de instalação.

![Image](/images/cd.jpg)

### Acesso Web Admin Endian Firewall

Acessaremos a interface gráfica do Endia através de um navegador, será necessário a utilização de uma maquina cliente. No seu navegador digite **https://endereipdoseuendian:10443**, no primeiro acesso você será informado que existe um problema de certificado. Basta clicar em continuar no site
não seguro.

![Image](/images/acess1.JPG)

**1** Após abrirá a janela inicial clique no botão >>> para continuar.

![Image](/images/acess2.JPG)

**2** Escolha o idioma e fuso horário e clique no botão >>> para continuar.

![Image](/images/acess3.jpg)

**3** Marque opção que aceita os termos e avance.

![Image](/images/acess4.jpg)

**4** Tela seguinte pergunta se você deseja restaurar uma cópia de segurança já existente, apenas clique
 no botão >>> para avençar.

![Image](/images/acess5.jpg)

**5** Na próxima janela defina as senhas de administração da interface web e senha de root para acesso
via SSH.

![Image](/images/acess6.jpg)

**6** Você deve configurar a ZONA VERMELHA de acordo com serviço fornecido pelo seu provedor de internet.
- ETHERNET STATIC A interface RED recebera um endereço IP estático.
- DHCP ETHERNET A interface RED recebe sua configuração de rede via DHCP (dinâmico).
- PPPoE A interface vermelha está ligado a um modem ADSL. Esta opção só é necessária quando o modem utiliza o modo de bridge e requer usar PPPoE para se conectar ao provedor.
- ADSL (USB, PCI) A interface RED se conecta a um modem ADSL através de um cabo USB ou PCI.
- ISDN A interface VERMELHO é uma ligação RDIS.

![Image](/images/acess7.jpg)

**7** Apenas avence janela de configuração das redes LARANJA E AZUL.

![Image](/images/acess8.jpg)

**8** Configuração da ZONA VERDE endereço que configuramos na instalação caso queira alterar escolha um novo endereçamento e máscara, digite nome do grupo de trabalho ou
AD.

![Image](/images/acess9.jpg)

**9** Próxima configuração escolha servidor DNS para Endian, clique no botão >>> até chegar na opção
OK, APPLY CONFIGURATION para finalizar.

![Image](/images/acess10.jpg)

**10** Aguarde um minuto será exibida tela de login do Endian, digite usuário *admin* e senha que foi definida no passo *5*. Endian solicita que você digite endereço de e-mail, apenas ignore clicando em I DON´T WANT ANY UPDATES.

![Image](/images/acess11.jpg)

**11** O Dashboard é a página padrão, organizada em duas colunas que fornecem uma visão completa do sistema. As informações visíveis na tela são atualizados em intervalos regulares.

![Image](/images/acess12.jpg)

### Status do Sistema

As páginas de status apresenta uma lista completa de informações sobre o estado atual do seu Endian Firewall. A primeira subseção, Status do sistema:
- **Serviços:** Exibe os serviços que estão atualmente em execução.
- **Memória:** Exibe o uso swapfile de memória.
- **Uso de disco:** Mostra a saída do df, que relata a quantidade de total (Tamanho), usado e espaço livre em disco.
- **Uptime e Usuários:** Exibe a saída do w comando que informa o tempo atual, informações sobre o tempo que o sistema tem funcionado sem reinicialização.
- **Módulos carregados:** Isso exibe todos os módulos atualmente carregados e em uso pelo kernel.
- **Kernel Versão:** Exibe informações sobre o próprio Kernel do Endian. Ele exibe versão do kernel.

![Image](/images/status1.jpg)

* Status de Rede exibe informações sobre todos os seus dispositivos de rede. Isto inclui PPP, OpenVPN, IPSec, auto-retorno, etc. Basicamente, isto é a saída de ifconfig.

![Image](/images/status2.jpg)

* Gráficos sistema clique em um dos gráficos (uso da CPU, uso de memória, uso de troca e acesso ao disco) para obter gráficos de uso por dia, semana, mês e ano.

![Image](/images/status3.jpg)

* Tráfego Gráficos esta página dá uma descrição gráfica do tráfego de entrada e de saída. Há seções para cada interface de rede, Verde e Vermelho (Azul e laranja se configurado). Clique em um dos gráficos para mostrar mais gráficos do tráfego nessa interface: por dia, semana, mês e ano.

![Image](/images/status4.jpg)

* Gráficos Proxy mostra o tráfego que passou pelo serviço de proxy. Esta informação é útil se o proxy tem o tamanho correto para a carga que está sendo experimentado.

* Ligações Endian Firewall utiliza a instalação firewall Linux Netfilter ou IPTables para manter um firewall stateful. O controle de conexões para todas as ZONAS, com base em ambos os endereços IP de origem e de destino e portas.

![Image](/images/status5.jpg)

* Estatísticas de correio SMTP esta página mostra estatísticas gráficos sobre o proxy SMTP Mail.

* Mail Queue exibe a fila de correio atual.

### Network

Esta página é projetada para ajudá-lo a administrar configuração relacionada a rede. Permite configurar entradas de host personalizado. Endian Firewall está executando um proxy DNS chamada dnsmasq, que encaminha todos os pedidos de resolução DNS do seu uplink RED. Isto é muito útil se você quiser criar nomes de máquinas que podem ser resolvidos apenas por seus clientes, mas não pode configurá-los diretamente no seu servidor DNS.

![Image](/images/network/net1.jpg)

- Editor de rotas estáticas é possibilita criar rotas especificas para um endereçamento IP, porta ou uplink especifico.

![Image](/images/network/net2.jpg)

- Gerenciamento de uplink esta página você pode criar regras de failover dos uplinks.

![Image](/images/network/net3.jpg)
