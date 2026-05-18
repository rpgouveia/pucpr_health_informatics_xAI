# PUCPR Health Informatics - Explainable AI (xAI)

Um projeto educacional sobre **Inteligência Artificial Explicável** aplicada a problemas de saúde, desenvolvido na Pontifícia Universidade Católica do Paraná.

## Visão Geral

Este projeto demonstra a importância da interpretabilidade em modelos de aprendizado de máquina, particularmente no contexto da saúde, onde decisões precisam ser compreendidas e justificadas.

Usando o dataset clássico de **Câncer de Mama (UCI Breast Cancer)**, o projeto compara:

1. **Modelos Interpretáveis** (Árvore de Decisão) - fáceis de entender, mas com performance moderada
2. **Modelos Black-Box** (Redes Neurais) - melhor performance, mas pouco transparentes
3. **Técnicas de Explicabilidade** (SHAP, LIME) - explicações para modelos complexos

## Objetivos

- Compreender a diferença entre modelos interpretáveis e black-box
- Explorar técnicas de explicabilidade (SHAP, LIME)
- Aplicar conceitos de xAI em um contexto de saúde
- Demonstrar por que a interpretabilidade é crítica em domínios sensíveis

## Estrutura do Projeto

```
├── example1-decision-tree.ipynb          # Modelo interpretável: Árvore de Decisão
├── example2-mlp-black-box.ipynb          # Modelo black-box: Rede Neural (MLP)
├── example3-mlp-shap-lime.ipynb          # Técnicas de explicabilidade: SHAP e LIME
├── data-mining-env-linux.yml             # Dependências para Linux
├── data-mining-env-windows.yml           # Dependências para Windows
├── output/                               # Resultados e visualizações
├── LICENSE                               # Licença do projeto
└── README.md                             # Este arquivo
```

## Descrição dos Notebooks

### 1. Example 1: Decision Tree (`example1-decision-tree.ipynb`)

Demonstra um modelo **interpretável e transparente**:
- Carregamento e exploração do dataset
- Treinamento de uma árvore de decisão
- Visualização da estrutura interna do modelo
- Matriz de confusão e métricas de desempenho

**Principais conceitos:** Interpretabilidade intrínseca, visualização de modelos

---

### 2. Example 2: MLP Black-Box (`example2-mlp-black-box.ipynb`)

Explora um modelo **neural de alta performance, mas pouco interpretável**:
- Setup do dataset com normalização
- Treinamento de uma rede neural (MLP - Multi-Layer Perceptron)
- Análise de pesos e limitações da interpretabilidade
- Avaliação de desempenho
- Demonstração de por que "abrir a caixa-preta" é desafiador

**Principais conceitos:** Modelos complexos, limitações de interpretabilidade, importância de xAI

---

### 3. Example 3: Explicabilidade com SHAP e LIME (`example3-mlp-shap-lime.ipynb`)

Apresenta **técnicas modernas para explicar modelos black-box**:
- Explicabilidade global com **SHAP (SHapley Additive exPlanations)**
  - Feature importance baseado em teoria dos jogos
  - SHAP values para diferentes samples
  - Visualizações: force plots, dependence plots, beeswarm plots
  
- Explicabilidade local com **LIME (Local Interpretable Model-agnostic Explanations)**
  - Explicações per-sample
  - Aproximações locais de modelos globais
  - Análise de contribuição de features

**Principais conceitos:** SHAP, LIME, explicabilidade local vs global, feature importance

---

## Pré-requisitos

- **Python 3.8+**
- **Conda** (Anaconda ou Miniconda)
- Jupyter Notebook ou JupyterLab

## Instalação

### 1. Clone o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd pucpr_health_informatics_xAI
```

### 2. Crie o ambiente conda

**Para Linux/macOS:**
```bash
conda env create -f data-mining-env-linux.yml
conda activate data-mining
```

**Para Windows:**
```bash
conda env create -f data-mining-env-windows.yml
conda activate data-mining
```

### 3. Inicie o Jupyter

```bash
jupyter notebook
```

Ou use JupyterLab:
```bash
jupyter lab
```

## Como Usar

1. Abra os notebooks na ordem sugerida:
   - Comece com `example1-decision-tree.ipynb`
   - Depois `example2-mlp-black-box.ipynb`
   - Finalize com `example3-mlp-shap-lime.ipynb`

2. Execute as células sequencialmente para ver:
   - Treinamento dos modelos
   - Visualizações das estruturas
   - Gráficos de explicabilidade

3. Os resultados são salvos em `output/`:
   - Imagens das árvores de decisão
   - Gráficos de performance
   - Visualizações de SHAP e LIME

## Dataset

**Breast Cancer (UCI Machine Learning Repository)**
- **Classes:** 2 (Maligno vs. Benigno)
- **Amostras:** 569
- **Features:** 30 características médicas
- **Divisão:** 2/3 treino, 1/3 teste (random_state=42)

## Tecnologias Utilizadas

| Tecnologia | Descrição |
|-----------|-----------|
| **scikit-learn** | Modelos de ML (Árvore, MLP, métricas) |
| **pandas** | Manipulação de dados |
| **numpy** | Computação numérica |
| **matplotlib** | Visualizações básicas |
| **SHAP** | Explicabilidade global (SHapley values) |
| **LIME** | Explicabilidade local |
| **seaborn** | Visualizações avançadas |

## Conceitos-Chave

- **Interpretabilidade:** Capacidade de entender por que um modelo faz uma previsão
- **Transparência:** Clareza sobre o funcionamento interno do modelo
- **xAI (Explainable AI):** Disciplina que visa tornar modelos de IA mais compreensíveis
- **SHAP:** Usa teoria dos jogos para atribuir importância a features
- **LIME:** Aproxima modelos complexos localmente com modelos simples
- **Black-Box:** Modelos cuja lógica interna não é facilmente interpretável

## Contexto de Saúde

Em aplicações médicas, a interpretabilidade é **fundamental**:
- Profissionais de saúde precisam entender decisões de IA
- Regulamentações requerem explicabilidade
- Confiança do paciente depende de transparência
- Erros podem ter impacto severo

Este projeto ilustra como técnicas de xAI tornam modelos adequados para contextos sensíveis.

## Referências

- [SHAP Documentation](https://shap.readthedocs.io/)
- [LIME GitHub](https://github.com/marcotcr/lime)
- [Interpretable Machine Learning - Christoph Molnar](https://christophm.github.io/interpretable-ml-book/)
- [UCI Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(diagnostic))

## Licença

Este projeto é fornecido sob a licença especificada em [LICENSE](LICENSE).

## Autores

- Renato Gouveia
- Márcia Cristina

---

**Nota:** Este é um projeto educacional. Use para aprender, pesquisar e compreender xAI. Para aplicações médicas reais, sempre consulte especialistas e siga regulamentações vigentes.