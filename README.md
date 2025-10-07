# 🎯 Classificação de Perfis de Investidores através de 'inputs'

Este projeto realiza a classificação automática de perfis de investidores a partir de dados textuais, utilizando processamento de linguagem natural e regras de negócio específicas.

## Sobre o Case

O objetivo deste projeto é criar um pipeline de classificação que:

1. **Processa dados textuais** de objetivos de investimento
2. **Classifica automaticamente** em categorias pré-definidas
3. **Define perfis de investidores** baseados nas classificações
4. **Gera relatórios agregados** para análise estratégica

## Estrutura do Projeto

### Pipeline de Classificação (`Case_Pipiline.ipynb`)
- Processa dados brutos do Excel
- Classifica objetivos de investimento usando fuzzy matching
- Identifica valores de aporte com regex
- Aplica hierarquia entre classificações (Objetivo > Resgate)
- Gera arquivo intermediário classificado

### Definição de Perfis (`Case_PerfisAgrupados.ipynb`)
- Filtra dados classificados pelo pipeline anterior
- Agrupa combinações de objetivos, aportes e resgates
- Aplica regras de negócio para mapear perfis de investidores
- Gera base final agregada para análise

### Dicionários de Classificação
- `objetivos_categorizados.json`: Mapeamento de termos para categorias de objetivos
- `resgate_categorizado.json`: Mapeamento de termos para intenção de resgate
  
## Tecnologias Utilizadas
- Python 3.x
- Pandas (manipulação de dados)
- FuzzyWuzzy (similaridade textual)
- OpenPyXL (manipulação de Excel)
- JSON (configurações e dicionários)
- 
## Como funciona

- Dados Brutos (data/Case - Wpp.xlsx)
- ↓
- [src/1.pipeline_classificacao.py]
- ↓
- Dados Classificados (results/Case - Wpp_PIPELINE_CLASSIFICADO_final.xlsx)
- ↓
- [src/2.definicao_perfis.py]
- ↓
- Perfis Agregados (results/base_perfis_agrupados.xlsx)

##Arquivos de Configuração
- requirements.txt - Dependências do projeto
- .gitignore - Arquivos ignorados pelo Git
- LICENSE - Licença do projeto


### Pré-requisitos
```bash
pip install -r requirements.txt

## Estrutura de Arquivos
- src/1.pipeline_classificacao.py - Pipeline principal de classificação
- src/2.definicao_perfis.py - Definição de perfis de investidores
- src/*.json - Dicionários para classificação textual
- src/*.ipynb - Notebooks para análise interativa
## Arquivos de Configuração
- requirements.txt - Dependências do projeto
- .gitignore - Arquivos ignorados pelo Git
- LICENSE - Licença do projeto
