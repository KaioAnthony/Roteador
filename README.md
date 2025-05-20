# __TL-WR940N__

![](https://images.tcdn.com.br/img/img_prod/571937/roteador_wireless_n_450mbps_tl_wr940n_c_3_ant_tp_link_3495_1_20240430195102.png)

### 
A seguir está um guia completo e passo a passo para configurar o roteador TP-Link TL-WR940N. Nele você encontrará desde a instalação física até ajustes avançados de segurança e atualização de firmware, tudo detalhado para garantir que sua rede Wi-Fi funcione de forma estável e segura.
### 

## Pré-requisitos

* **Manual e firmware:**

  * Acesse o site oficial TP-Link e, na seção de suporte do modelo TL-WR940N, baixe o Manual de Usuário correspondente à sua versão de hardware (V6, V6.6 etc.).
  * Ainda na mesma página, faça o download do firmware mais recente. Salve-o em um local fácil de achar (ex.: Área de Trabalho).
* **Computador ou smartphone:**

  * Você pode usar tanto PC (Windows, macOS ou Linux) quanto smartphones/tablets (Android ou iOS).
  * Se for usar Wi-Fi, verifique se seu dispositivo não está configurado com IP fixo em outra faixa de rede.
* **Cabo de rede e fonte de alimentação:**

  * Utilize o cabo Ethernet fornecido para garantir boa qualidade de sinal.
  * Certifique-se de que a fonte está em boas condições e conecta corretamente na tomada.

## Passo 1 – Instalação física

1. **Posicionamento inicial**

   * Escolha um local central na casa, longe de eletrodomésticos (micro-ondas, TVs antigas, refrigeradores) e objetos metálicos que possam bloquear o sinal.
   * Mantenha o roteador em lugar ventilado, pois ele aquece durante o uso.
2. **Ligação da fonte**

   * Conecte a fonte à porta **Power** na traseira do roteador. O LED de **Power** deve piscar por alguns segundos e depois permanecer fixo em verde.
3. **Conexão ao modem/ONT**

   * Insira um extremo do cabo Ethernet na porta **WAN/Internet** (azul) do TL-WR940N e o outro extremo na porta LAN do seu modem ou ONT.
   * O LED **WAN** no roteador deve acender indicando tráfego de link.
4. **Conexão ao computador (opcional)**

   * Se desejar uma configuração mais estável, use outro cabo Ethernet para ligar a porta LAN 1 (ou 2, 3, 4) ao seu computador.
   * Caso prefira Wi-Fi, localize na etiqueta inferior do roteador o SSID (nome da rede) e a senha (Password). No primeiro acesso, a senha pode vir em branco ou ser “admin”.

## Passo 2 – Acessar a interface de administração

1. **Abrir navegador**

   * No campo de endereço, digite `http://tplinkwifi.net` ou o IP padrão `http://192.168.0.1`.
2. **Login inicial**

   * Usuário: **admin**
   * Senha: **admin**
   * Assim que entrar, você será solicitado a alterar a senha de administrador — é altamente recomendável fazer isso no primeiro acesso.
3. **Solução de problemas de acesso**

   * Se a página não carregar, verifique se seu adaptador de rede está obtendo IP via DHCP.
   * No Windows, desative eventuais proxies em *Painel de Controle > Internet Options > Connections > LAN Settings*.
   * Se ainda não funcionar, use `ipconfig` (Windows) ou `ifconfig` (Linux/Mac) para checar se seu gateway padrão é realmente 192.168.0.1.

## Passo 3 – Configurar conexão com a Internet (WAN)

1. **Localizar a seção**

   * No menu lateral, expanda **Network** e clique em **Internet** ou **WAN** (dependendo da versão de firmware).
2. **Selecionar tipo de conexão**

   * **Dynamic IP (IP Dinâmico):** seu provedor atribuirá um IP automaticamente.
   * **PPPoE:** para conexões ADSL; informe o nome de usuário e senha que seu provedor forneceu.
   * **Static IP:** insira manualmente o IP, Máscara de Sub-Rede, Gateway e servidores DNS.
3. **Configurações avançadas (opcionais)**

   * Em alguns firmwares você pode definir MTU e VLAN ID. Verifique com seu provedor se eles exigem um valor específico (ex.: VLAN 10 para IPTV).
4. **Salvar e testar**

   * Clique em **Save**.
   * Aguarde até 30 segundos e verifique o status de conexão – o campo “Internet” deverá exibir “Connected” e mostrar um IP válido.

## Passo 4 – Configuração da rede Wi-Fi

1. **Wireless Settings**

   * Vá em **Wireless > Wireless Settings**.
2. **Definições principais**

   * **Wireless Network Name (SSID):** escolha um nome que identifique facilmente sua rede.
   * **Region:** Brasil. Isto garante o uso correto dos canais permitidos.
   * **Channel Width:** deixe em **20/40 MHz** para maior compatibilidade ou em **20 MHz** se estiver em ambiente muito congestionado.
   * **Channel:** em “Auto” o roteador escolhe o melhor canal; para ambientes cheios, use apps de análise de Wi-Fi para selecionar um canal livre (ex.: 1, 6 ou 11 no 2,4 GHz).
3. **Salvar alterações**

   * Clique em **Save**.
   * Após salvar, sua rede pode reiniciar o rádio e dispositivos conectados serão desconectados momentaneamente.

## Passo 5 – Configuração de segurança

1. **Wireless Security**

   * Acesse **Wireless > Wireless Security**.
2. **Tipo de criptografia**

   * Selecione **WPA/WPA2-Personal**.
   * **WPA2-PSK** com **AES** é o mais seguro e compatível.
3. **Senha de acesso**

   * Em **Password**, crie uma senha forte, combinando letras maiúsculas, minúsculas, números e símbolos (mínimo 8 caracteres).
4. **Aplicar e testar**

   * Clique em **Save**.
   * Reconecte seus dispositivos usando a nova senha para confirmar o funcionamento.

## Passo 6 – DHCP e LAN

1. **Alterar IP interno (se necessário)**

   * Em **Network > LAN**, você pode mudar o IP do roteador (ex.: de 192.168.0.1 para 192.168.2.1) para evitar conflitos com outra rede local.
2. **Configurar servidor DHCP**

   * Em **DHCP > DHCP Settings**, defina:

     * **DHCP Server:** Enabled.
     * **Start IP Address:** por exemplo, 192.168.0.100.
     * **End IP Address:** por exemplo, 192.168.0.199.
     * **Lease Time:** tempo de “aluguel” do IP, ex.: 1440 min (24 h).
3. **Reserva de IP (opcional)**

   * Use o recurso **Address Reservation** para que dispositivos específicos (impressora, NAS) sempre recebam o mesmo IP.
4. **Salvar**

   * Clique em **Save** e, se alterou o IP do roteador, reconecte-se ao novo gateway.

## Passo 7 – Atualização de firmware

1. **Download do firmware**

   * Confirme a versão de hardware (etiqueta embaixo do roteador) e baixe o arquivo exato no site TP-Link.
2. **Entrar na seção de upgrade**

   * Vá em **System Tools > Firmware Upgrade**.
3. **Processo de atualização**

   * Clique em **Browse**, selecione o arquivo `.bin` baixado e depois **Upgrade**.
   * Não desligue o roteador, nem recarregue a página. A atualização leva cerca de 2–3 min.
4. **Verificar versão**

   * Após reiniciar, em **System Tools > System Info**, confirme se a “Firmware Version” foi atualizada corretamente.

## Passo 8 – Salvar configurações e reiniciar

1. **Reboot do sistema**

   * Em **System Tools > Reboot**, clique em **Reboot** para garantir que todas as configurações entraram em vigor sem erros.
2. **Backup das configurações**

   * Em **System Tools > Backup & Restore**, clique em **Backup** para baixar um arquivo de configuração (.bin).
   * Guarde-o em local seguro; você poderá restaurar em **Restore** caso precise reconfigurar do zero no futuro.

---

**Dicas adicionais:**

* **Alterar credenciais de administrador:**

  * Em **System Tools > Password**, troque o usuário “admin” e a senha padrão por algo único.
* **Controlar acesso de usuários:**

  * Use **Access Control** para filtros de MAC, horário de acesso ou bloqueio de sites (URL Filtering, Keyword Filtering).
* **Modo de operação:**

  * Em firmwares que oferecem **Operation Mode**, você pode alternar para **Range Extender**, **Access Point** ou **WISP**, adaptando o roteador a diferentes cenários de uso.
* **Monitoramento e logs:**

  * Verifique em **System Tools > System Log** as mensagens de sistema para diagnosticar erros.
* **Posicionamento ideal:**

  * Antenas sempre viradas para cima e distância mínima de 1 metro de outros dispositivos eletrônicos.
### 
