<div align="center">

# 🌐 Laboratório Virtual de Redes

### IPv4 • CIDR • Máscaras • Subnetting • VLSM • DHCP • Gateway • IPv6

**Aprenda endereçamento IP com cálculos interativos e explicações passo a passo.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) ![Educação](https://img.shields.io/badge/Projeto-Educacional-2563EB) ![Status](https://img.shields.io/badge/Status-Em%20evolu%C3%A7%C3%A3o-22A06B)

**Teclabs Info · Desenvolvimento: Anthony Freitas**

[LinkedIn](https://www.linkedin.com/in/tony-s-freitas/) · [GitHub Teclabs Info](https://github.com/TeclabsInfo) · [Portfólio](https://sammyfreitas.github.io/portfolioSite/) · [Contato](mailto:tonysdefreitas@gmail.com)

</div>

---



## 📝 Quiz de redes — rodadas e avaliação por tentativas

- A cada rodada, são sorteadas **até 10 questões**, sem repetição dentro da rodada. No filtro **Todos os níveis**, são 10 dentre as 18 disponíveis. Os filtros individuais podem ter menos de 10 questões, pois o banco atual não tem 10 em cada nível.
- O aluno pode tentar novamente **quantas vezes precisar**. Cada tentativa incorreta é registrada, e a questão só é concluída quando a resposta correta é selecionada.
- Após acertar, a questão é bloqueada para evitar contagens repetidas e a explicação é exibida.
- A tela mostra questões resolvidas, tentativas, erros, percentual de aproveitamento e nota equivalente de 0 a 10.
- **Aproveitamento = (questões acertadas ÷ total de tentativas) × 100**; **nota = aproveitamento ÷ 10**. Ex.: 10 acertos em 13 tentativas = 76,92% e nota 7,69.
- O botão **Sortear nova rodada de 10** reinicia o placar da rodada e sorteia novamente; o filtro de nível também inicia uma nova rodada. As questões podem reaparecer em rodadas futuras.
- A pontuação é **formativa**, não identifica alunos e não é armazenada após recarregar a página.

## 🩺 Diagnóstico IPv4 e terminal didático (v2.0 / v2.1 parcial)

- **Diagnóstico de configuração:** informe IP, máscara/CIDR, gateway e DNS. O laboratório verifica sintaxe, máscara contígua, endereços de rede e broadcast, gateway fora da sub-rede e alguns endereços especiais. Cada resultado explica como corrigir o problema. O diagnóstico não mede conectividade real nem comprova funcionamento do DNS. Prefixos `/31` e `/32` têm usos especiais e não recebem a regra comum de hosts.
- **Terminal simulado Windows/Linux:** `ipconfig`, `ipconfig /all`, `ip addr`, `ping DESTINO`, `tracert DESTINO`, `traceroute DESTINO`, `nslookup NOME` e `arp -a`. Os resultados são **fictícios e educativos**. Nenhum comando é executado no computador e nenhum pacote é transmitido.
- **Enviar para outra ferramenta:** a análise IP/CIDR, o simulador de gateway e o mapa VLSM enviam uma configuração ao diagnóstico. O diagnóstico permite continuar no terminal. Confira o gateway sugerido antes de aplicar em redes reais.

### Exemplo de diagnóstico

- IP: `192.168.1.50`
- Máscara: `/24`
- Gateway: `192.168.2.1`
- DNS: `1.1.1.1`

O gateway informado está fora da rede local `192.168.1.0/24`, portanto não é um próximo salto diretamente alcançável na configuração convencional.

### Status do roteiro

| Versão | Entrega | Estado |
| --- | --- | --- |
| 2.0 | Diagnóstico de IP/máscara/gateway/DNS | Implementado (análise estática) |
| 2.0 | Compartilhamento de dados entre calculadoras | Parcial: IP/CIDR, gateway, VLSM visual → diagnóstico → terminal |
| 2.0 | Erros com explicações e sugestões | Implementado nos novos recursos |
| 2.1 | Terminal Windows/Linux simulado | Implementado |
| 2.1 | Missões de suporte progressivas | Pendente |
| 2.1 | Pontuação e feedback das missões | Pendente |
| 2.2 | Montador interativo de topologias | Pendente; existe visualizador de topologia e caminho |
| 2.2 | Salvar/carregar planejamentos | Pendente |
| 2.2 | Exportação de inventário e documentação | Pendente; há cópia textual do VLSM |
| 2.3 | Navegação completa por teclado | Pendente de auditoria e ajustes |
| 2.3 | Modo projetor | Pendente |
| 2.3 | Histórico local e retomada | Pendente |

## 🗺️ Planejamento visual de redes

A evolução do laboratório inclui duas ferramentas interativas, acessíveis pelo menu **Planejamento de redes**:

### Mapa visual de sub-redes (VLSM)

- Informe uma rede de origem, como `192.168.10.0/24`.
- Cadastre setores no formato `Nome; quantidade de dispositivos`, um por linha.
- O laboratório distribui os blocos do maior para o menor, respeitando os limites de CIDR e evitando sobreposição.
- Visualize a ocupação proporcional dos endereços, os intervalos de hosts, o broadcast, a máscara e o espaço restante.
- Copie o planejamento em texto para usar em exercícios ou documentações.

**Exemplo:** Administrativo (50) → `192.168.10.0/26`; Financeiro (25) → `192.168.10.64/27`; TI (10) → `192.168.10.96/28`.

### Topologia e caminho do pacote

- Informe IP de origem, IP de destino, prefixo e gateway.
- Observe os equipamentos em um diagrama simples (computador, switch e, quando necessário, roteador).
- Veja a decisão de entrega local via ARP ou de encaminhamento pelo gateway, com explicação passo a passo.
- Teste cenários com computadores na mesma sub-rede ou em redes diferentes.

**Importante:** são simulações conceituais. Não enviam pacotes reais, não configuram equipamentos e não substituem testes de conectividade, roteamento, VLANs ou regras de firewall.

## 📚 Sobre o projeto

O **Laboratório Virtual de Redes** é uma ferramenta educacional interativa desenvolvida para apoiar o ensino e a aprendizagem de **endereçamento IPv4, máscaras de sub-rede e planejamento de redes**.

O projeto surgiu da prática docente: em vez de apenas mostrar o resultado de uma conta, o laboratório ajuda o estudante a compreender **de onde vêm os números**, como os bits formam a máscara e como determinar a quantidade de endereços de uma sub-rede.

Foi pensado para uso em aulas presenciais, estudos individuais, demonstrações projetadas e preparação para atividades em simuladores de redes, como o Cisco Packet Tracer.

## 🧮 Funcionalidades

| Ferramenta | O que faz |
|---|---|
| **Máscara → Hosts** | Recebe uma máscara IPv4, identifica o CIDR e calcula os endereços totais e utilizáveis. |
| **Hosts → Máscara** | Encontra a menor sub-rede convencional que atende à quantidade solicitada de hosts. |
| **IP + CIDR** | Calcula endereço de rede, broadcast, intervalo de hosts e máscara. |
| **Subnetting** | Auxilia na divisão de um bloco em sub-redes menores. |
| **VLSM** | Planeja sub-redes com tamanhos diferentes conforme as necessidades dos setores. |
| **Comparador de IPs** | Verifica se dois endereços pertencem à mesma sub-rede. |
| **Binário ↔ Decimal** | Demonstra a conversão entre bases numéricas usada no endereçamento IPv4. |

### 💻 Terminal explicativo

As ferramentas incluem explicações em formato de **terminal**, com etapas de cálculo e representações binárias. A tabela de potências de 2 é apresentada em ordem decrescente, de **2¹⁶ a 2⁰**, para acompanhar o raciocínio utilizado em aula.

Ao informar uma máscara inválida, o laboratório explica a regra dos **bits 1 consecutivos, seguidos por bits 0**. A representação binária ajuda a localizar o erro; após tentativas incorretas, são apresentados exemplos dos valores possíveis em um octeto de máscara: **0, 128, 192, 224, 240, 248, 252, 254 e 255**.

> **Atenção:** esses valores não podem ser combinados em qualquer ordem. Uma máscara válida deve manter os bits `1` contínuos a partir da esquerda.

## 🔎 Exemplos de uso

**Exemplo 1 — Máscara para quantidade de hosts**

```text
Necessidade:       1.500 hosts
CIDR:              /21
Máscara:           255.255.248.0
Endereços totais:  2.048
Hosts utilizáveis: 2.046
```

**Exemplo 2 — Análise de IP e CIDR**

```text
Entrada:           192.168.100.20/29
Máscara:           255.255.255.248
Endereço de rede:  192.168.100.16
Primeiro host:     192.168.100.17
Último host:      192.168.100.22
Broadcast:         192.168.100.23
Hosts utilizáveis: 6
```

**Exemplo 3 — Conversão de máscara**

```text
Máscara decimal: 255.255.255.0
Máscara binária: 11111111.11111111.11111111.00000000
CIDR:            /24
```

## 🚀 Como executar

Não é necessário instalar Node.js, frameworks ou bibliotecas.

1. Baixe ou clone o repositório.
2. Abra o arquivo **`index.html`** em um navegador moderno.
3. Escolha a calculadora, preencha os campos e consulte o resultado.
4. Abra o terminal explicativo para acompanhar a resolução.

```bash
git clone https://github.com/SEU-USUARIO/laboratorio-virtual-redes.git
cd laboratorio-virtual-redes
```

> Substitua `SEU-USUARIO` pelo proprietário real do repositório após a publicação.

## 🌍 Publicação no GitHub Pages

Como o projeto é estático, pode ser hospedado gratuitamente no GitHub Pages:

1. No repositório, abra **Settings → Pages**.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Selecione a branch **main** e a pasta **/(root)**.
4. Salve e aguarde a publicação.

O endereço normalmente seguirá o formato `https://SEU-USUARIO.github.io/laboratorio-virtual-redes/`.

## 🎓 Proposta pedagógica

O laboratório foi concebido como **recurso de apoio ao aprendizado**, e não apenas como uma calculadora de respostas. Entre os objetivos estão:

- Relacionar endereço IPv4, máscara e notação CIDR.
- Interpretar os bits de rede e de host.
- Compreender as potências de 2 e a conversão binária.
- Calcular capacidade, rede, broadcast e intervalo de hosts.
- Planejar divisões de redes com subnetting e VLSM.
- Preparar os alunos para a configuração prática de dispositivos.

**Nota técnica:** a regra `2ⁿ − 2` é utilizada para sub-redes IPv4 convencionais. Os prefixos `/31` e `/32` exigem tratamento específico.

## 🛠️ Tecnologias

- **HTML5** — estrutura e acessibilidade semântica.
- **CSS3** — layout responsivo e temas claro/escuro.
- **JavaScript** — cálculos, validações e interatividade no navegador.

O projeto não exige backend nem banco de dados para executar suas calculadoras.

## 🧭 Evoluções planejadas

- Simulações didáticas de gateway e DHCP.
- Ferramentas introdutórias para IPv6.
- Exercícios com correção e feedback explicativo.
- Recursos visuais adicionais para planejamento de redes.

Esses itens são **possibilidades futuras**, não funcionalidades já disponíveis nesta versão.

## 👨‍💻 Autoria

**Anthony Freitas** — Desenvolvedor de Software e Professor

Projeto educacional desenvolvido sob a identidade **Teclabs Info**, com foco na aplicação prática da tecnologia ao ensino.

[LinkedIn](https://www.linkedin.com/in/tony-s-freitas/) · [GitHub](https://github.com/TeclabsInfo) · [Portfólio](https://sammyfreitas.github.io/portfolioSite/)

---

<div align="center">

**© 2026 Anthony Freitas · Teclabs Info. Todos os direitos reservados.**

</div>


### Navegação e limpeza de dados

Cada ferramenta possui o botão **↺ Limpar campos**, que apaga seus dados de entrada e resultados sem alterar as outras ferramentas. Os menus suspensos fecham automaticamente após a escolha de uma opção, ao clicar fora deles ou ao pressionar **Esc**.
