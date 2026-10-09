# Laboratório de Estudos: Lógica de Dados e Estatística com Python e SQL

Este repositório foi criado para documentar meus estudos práticos na transição da Engenharia Mecatrônica para a área de Dados/Machine Learning. O objetivo aqui foi aplicar lógica de programação (Python/SQL) e conceitos de estatística básica em problemas práticos de mercado.

---

## Ferramentas que usei nos testes
* **Python & Pandas:** Para limpar e transformar as tabelas.
* **SQLite:** Para simular consultas de banco de dados direto na memória do Jupyter Notebook.
* **NumPy:** Para gerar dados simulados e testar as regras.

---

## O que eu resolvi nesses exercícios:

### 1. Filtro de Fraude (Desvio Padrão)
* **O problema:** Bloquear transações suspeitas em um cartão de crédito.
* **Como resolvi:** Usei a média de gastos do cliente e calculei a barreira de 3 Desvios Padrões (Média + 3x Desvio Padrão). Criei uma query SQL que isola automaticamente qualquer compra que passe desse valor limite.

### 2. Média vs Mediana (Análise de Faturamento)
* **O problema:** Entender como valores extremos (outliers) distorcem relatórios.
* **Como resolvi:** Simulei uma base onde um único cliente corporativo gastava muito mais que os clientes comuns. Usei o método `.describe()` do Pandas para provar visualmente por que a Mediana reflete melhor a realidade do "cliente padrão" do que a Média nesse cenário.

### 3. Limpeza de Ruído de Sinais (Logs do Sistema)
* **O problema:** Tratar arquivos que vêm com erros técnicos de leitura (valores brutos como `-999.0`).
* **Como resolvi:** Exatamente como limpamos ruídos de sensores na mecatrônica, usei o Pandas para localizar esses códigos de erro, convertê-los em nulos (`NaN`) e limpar a tabela antes de salvar.

### 4. Exportação Automática
* **Como resolvi:** Usei a função `.to_csv(index=False)` para gerar o arquivo final limpo, garantindo que o Pandas não salvasse colunas vazias ou índices desnecessários.
