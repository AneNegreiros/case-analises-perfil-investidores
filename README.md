# 🎯 Classificação de Perfis de Investidores

Este projeto realiza a classificação automática de perfis de investidores a partir de dados textuais, utilizando processamento de linguagem natural e regras de negócio específicas.

## Sobre o Case

O objetivo deste projeto é criar um pipeline de classificação que:

1. **Processa dados textuais** de objetivos de investimento
2. **Classifica automaticamente** em categorias pré-definidas
3. **Define perfis de investidores** baseados nas classificações
4. **Gera relatórios agregados** para análise estratégica

## Estrutura do Projeto

### Pipeline de Classificação (`1.pipeline_classificacao.py`)
- Processa dados brutos do Excel
- Classifica objetivos de investimento usando fuzzy matching
- Identifica valores de aporte com regex
- Aplica hierarquia entre classificações (Objetivo > Resgate)
- Gera arquivo intermediário classificado

### Definição de Perfis (`2.definicao_perfis.py`)
- Filtra dados classificados pelo pipeline anterior
- Agrupa combinações de objetivos, aportes e resgates
- Aplica regras de negócio para mapear perfis de investidores
- Gera base final agregada para análise

### Dicionários de Classificação
- `objetivos_categorizados.json`: Mapeamento de termos para categorias de objetivos
- `resgate_categorizado.json`: Mapeamento de termos para intenção de resgate

## 🚀 Como Executar

### Pré-requisitos
```bash
pip install -r requirements.txt

## 🧩 Estrutura de Pastas
- scripts/ → códigos Python do pipeline
- data/ → bases de entrada e saída
- dicts/ → dicionários de regras JSON
- results/ → saídas tratadas
