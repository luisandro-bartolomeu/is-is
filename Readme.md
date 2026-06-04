# Protocolo de Roteamento Dinâmico IS-IS (Intermediate System to Intermediate System)

Trabalho escolar sobre o protocolo de roteamento dinâmico IS-IS, abordando a sua definição, arquitetura, história, comparação com outros protocolos, implementação prática e casos de uso no mundo real.

---

## 📋 Sobre o Trabalho

Este trabalho tem como objetivo principal compreender de forma aprofundada o protocolo **IS-IS (Intermediate System to Intermediate System)** , um protocolo de estado de enlace do tipo IGP amplamente utilizado nos backbones dos maiores Provedores de Serviço de Internet (ISPs) do mundo.

A pesquisa abrange desde as origens do protocolo nos laboratórios da Digital Equipment Corporation (DEC) na década de 1980, passando pela sua padronização pela ISO e adaptação para o TCP/IP, até à sua implementação prática em equipamentos Cisco e análise do seu nicho de aplicação no cenário atual de redes.

---

## 🎯 Objetivos

### Objetivo Geral
Compreender de forma aprofundada o protocolo de roteamento dinâmico IS-IS, analisando a sua arquitetura, funcionamento, contexto histórico e aplicabilidade no cenário de redes contemporâneo.

### Objetivos Específicos
- Definir o conceito de protocolo de roteamento dinâmico e situar o IS-IS neste contexto.
- Investigar a história do IS-IS, desde a sua conceção na DEC até à padronização e evolução.
- Comparar o IS-IS com RIP, EIGRP, OSPF e BGP, destacando vantagens e desvantagens.
- Demonstrar a implementação prática em roteadores Cisco.
- Identificar casos de uso reais e o nicho de mercado onde o IS-IS é predominante.

---

## 📚 Conteúdo do Trabalho

1. **Resumo** — Síntese dos principais pontos abordados.
2. **Introdução** — Contextualização do tema e justificativa do estudo.
3. **Objetivos** — Objetivo geral e objetivos específicos listados.
4. **Fundamentação Teórica**
   - Definição e classificação de protocolos de roteamento dinâmico.
   - Explicação do conceito de estado de enlace (Link-State).
   - Funcionamento do LSA/LSP e convergência.
   - Definição do IS-IS e origem do nome (terminologia OSI).
   - História detalhada com marcos temporais (1985–1990).
   - Comparação abrangente com RIP, EIGRP, OSPF e BGP.
   - Implementação prática em roteadores Cisco com comandos.
   - Casos de uso reais (ISPs, Data Centers, redes críticas).
5. **Conclusão** — Síntese das aprendizagens e importância do IS-IS.
6. **Bibliografia** — Referências académicas e técnicas utilizadas.

---

## 🖥️ Implementação Prática

O trabalho inclui uma demonstração completa de configuração do IS-IS em roteadores Cisco, simulando um ambiente real de Provedor de Serviço de Internet (ISP) com:

- **Roteador de Backbone (L2 Only)**
- **Roteador de Fronteira (L1/L2)**

### Topologia
[ R-Core-01 ] <--- Backbone L2 ---> [ R-PoP-01 ] <--- Área L1 ---> [Rede do Cliente]
.1 (G0/1) 10.0.0.0/30 .2 (G0/1) (G0/2) 192.168.1.0/24


### Comandos de verificação
```bash
show ip protocols        # Protocolos de roteamento ativos
show clns neighbors      # Vizinhos IS-IS e estado da adjacência
show isis database       # Base de dados de estado de enlace (LSDB)
show ip route isis       # Rotas IP aprendidas via IS-IS