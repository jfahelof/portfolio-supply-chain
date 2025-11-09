# 🚚 Otimização de Rotas com Pyomo e Mapas Reais

Um projeto integrado de pesquisa operacional que combina modelagem matemática com mapas reais para resolver problemas logísticos de distribuição de forma otimizada.

## 📋 Sobre o Projeto

Este trabalho desenvolve uma solução completa para problemas de distribuição logística, integrando mapas reais (OpenStreetMap) com modelagem matemática no Pyomo. O sistema resolve o problema clássico de como distribuir produtos de um Centro de Distribuição (CD) para diferentes locais de forma ótima, considerando:

- ✅ Demandas específicas de cada local
- ✅ Capacidades dos centros de distribuição  
- ✅ Distâncias reais entre os pontos
- ✅ Custos de transporte

### 🎯 Aplicações Práticas
- **Empresas de logística** - Otimização de frota e rotas
- **Varejo** - Distribuição para lojas físicas
- **Supply Chain** - Planejamento de rede de distribuição
- **Gestão Urbana** - Distribuição de recursos municipais

## 🛠 Tecnologias Utilizadas

| Tecnologia | Finalidade |
|------------|------------|
| **Pyomo** | Modelagem e solução do problema de otimização |
| **OSMnx + NetworkX** | Obtenção e análise de mapas reais |
| **Folium** | Visualização interativa das rotas |
| **GLPK** | Solver para otimização linear |
| **Python** | Integração e análise dos dados |

## 📊 Modelo Matemático Implementado

### Função Objetivo
Minimizar o custo total de transporte:

$$
\min z = \sum_{i=1}^{m} \sum_{j=1}^{n} c_{ij} \cdot x_{ij}
$$

### Restrições do Modelo

**1. Capacidade dos Fornecedores**
Não exceder a capacidade de cada origem $i$:

$$
\sum_{j=1}^{n} x_{ij} \leq a_i \quad \forall i \in \{1,2,...,m\}
$$

**2. Atendimento à Demanda**  
Satisfazer a demanda de cada destino $j$:

$$
\sum_{i=1}^{m} x_{ij} \geq b_j \quad \forall j \in \{1,2,...,n\}
$$

**3. Não-Negatividade**
$$
x_{ij} \geq 0 \quad \forall i,j
$$

### Estrutura do Problema

| Componente | Descrição |
|------------|-----------|
| **Variáveis de decisão** | $x_{ij}$ = quantidade transportada da origem $i$ para o destino $j$ |
| **Parâmetros** | $c_{ij}$ = custo unitário de transporte |
| | $a_i$ = capacidade da origem $i$ |
| | $b_j$ = demanda do destino $j$ |

## 🎯 Resultados e Capacidades

### Funcionalidades Principais
- **🎯 Otimização de Rotas** - Identifica as melhores rotas e quantidades a enviar
- **⚖️ Balanceamento de Recursos** - Garante que capacidades e demandas sejam respeitadas
- **📍 Localização Ótima** - Identifica o melhor local para instalar novos CDs
- **📈 Escalabilidade** - Lida com problemas de pequeno a grande porte

### Características do Modelo
- 🔹 **Programação Linear** - Estrutura matemática eficiente e comprovada
- 🔹 **Problema Balanceado** - Quando $\sum a_i = \sum b_j$
- 🔹 **Soluções Ótimas** - Garantia de minimização de custos
- 🔹 **Aplicação Real** - Usa distâncias reais de redes viárias

## 💡 Impacto e Aplicabilidade

Este projeto demonstra o poder da **Ciência de Dados aplicada à Logística**, unindo:
- **Teoria** - Fundamentos de pesquisa operacional
- **Programação** - Implementação prática e escalável  
- **Tomada de Decisão** - Resultados acionáveis para negócios

Exatamente o tipo de solução que impulsiona a **eficiência operacional** no mundo real, reduzindo custos e melhorando o serviço ao cliente.

---

*Integrando mapas reais com otimização matemática para decisões logísticas inteligentes.*
