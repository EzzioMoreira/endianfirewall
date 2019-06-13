## Edian Firewall

O Endian Firewall é uma [distribuição Linux](https://pt.wikipedia.org/wiki/Distribui%C3%A7%C3%A3o_Linux) especializada em roteamento/firewall que possui uma interface unificada de gerenciamento. Foi desenvolvido pela italiana [Endian Srl](https://pt.wikipedia.org/w/index.php?title=Societ%C3%A0_a_Responsabilit%C3%A0_Limita&action=edit&redlink=1) e pela comunidade.

O Endian Firewall foi originalmente baseado no [IPCop](https://pt.wikipedia.org/wiki/IPCop), sendo que este é um fork do projeto [Smoothwall](http://en.wikipedia.org/wiki/SmoothWall). [Wikipédia](https://pt.wikipedia.org/wiki/Endian_Firewall).
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


- **VERMELHA**, este é o chamado segmento não confiável, ou seja, a WAN: Abrange todas as redes fora do Endian, em termos gerais, a Internet, e é a fonte de conexões de entrada.

- **VERDE**, a rede interna, ou seja, a LAN. Esta zona é a mais protegida e é dedicado às estações de trabalho e nunca deve ser acessado diretamente a partir da zona vermelha. É também a única zona que, por padrão pode acessar a interface de gerenciamento.

- **LARANJA**, ou **DMZ**, esta zona deve hospedar os servidores que precisam acessar a Internet para fornecer serviços (por exemplo, SMTP / POP, SVN e HTTP). Se um invasor consegue quebrar um dos serviços/servidores, o mesmo ficará preso dentro da DMZ e não será capaz atingir a zona verde.

- **AZUL**, zona Wi-Fi, ou seja, a zona que deve ser usado por clientes sem fio para acessar a Internet. As redes sem fio, muitas vezes não são seguras, então a ideia é isolar todos os clientes conectados sem fio em sua própria zona sem acesso a qualquer outra zona, exceto RED.


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
