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
Acessaremos a interface gráfica do Endia através de um navegador, será necessário a utilização de uma maquina cliente. No seu navegador digite https://endereipdoseuendian:10443, no primeiro acesso você será informado que existe um problema de certificado. Basta clicar em continuar no site não seguro.
![Image](/images/acess1.jpg)

**1** Após abrirá a janela inicial clique no botão >>> para continuar.

![Image](/images/acess2.jpg)

**2** Escolha o idioma e fuso horário e clique no botão >>> para continuar.

![Image](/images/acess3.jpg)

**3** Marque opção que aceita os termos e avance.
![Image](/images/acess4.jpg)

**4** Tela seguinte pergunta se você deseja restaurar uma cópia de segurança já existente, apenas clique no botão >>> para avençar.
![Image](/images/acess5.jpg)

**5** Na próxima janela defina as senhas de administração da interface web e senha de root para acesso via SSH.

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

**8** Configuração da ZONA VERDE endereço que configuramos na instalação caso queira alterar escolha um novo endereçamento e máscara, digite nome do grupo de trabalho ou AD.
![Image](/images/acess9.jpg)

**9** Próxima configuração escolha servidor DNS para Endian, clique no botão >>> até chegar na opção OK, APPLY CONFIGURATION para finalizar.
![Image](/images/acess10.jpg)



O Dashboard é a página padrão organizados em duas colunas que fornecem uma visão completa do sistema de marcha e da sua saúde. A parte superior de cada caixa relata o nome da caixa. O Painel ultimamente tem sofrido algumas alterações em sua usabilidade e novos recursos foram adicionados para melhorar a interação com o usuário. As informações visíveis na tela são atualizados em intervalos regulares.



```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/EzzioMoreira/endianfirewall/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
