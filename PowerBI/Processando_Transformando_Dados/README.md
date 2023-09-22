## Desafio Processando e Transformando Dados com Power BI

### **Etapas do desafio:**

1. Criação de uma instância na Azure para MySQL;
2. Criação do Banco de dados com base disponível no Github [julianazanelatto/power_bi_analyst/Módulo 3/Desafio de Projeto](https://github.com/julianazanelatto/power_bi_analyst/tree/main/M%C3%B3dulo%203/Desafio%20de%20Projeto);
3. Integração do Power BI com MySQL no Azure;
4. Transformação de dados no Power Query do Power BI;
5. Criação de relatório com os dados transformados.

### Transformação de dados realizadas:

* Tabela *Company Employee*:
    * Mescla das colunas de nome e sobrenome;
    * Divisão da coluna de endereço em número, rua, cidade e estado;
    * Alteração do tipo de dados da coluna de salários para número decimal fixo;
    * Inclusão de 'CEO' para o colaborador James E Borg na coluna Super_ssn, pois ele não possui gerente então é possível concluir que ele tenha o cargo mais elevado na empresa.

* Mescla das tabelas *Company Employee* e *Departament*:
    * Criação de uma nova consulta *Employee x Departament* com os dados dos colaboradores e seu respectivo departamento;
    * Exclusão das colunas desnecessárias desta nova tabela, mantendo apenas os dados de nome do colaborador e departamento.

* Mescla das colunas *Super_ssn* e *Ssn* da tabela *Company Employee* para identificar os gerentes de cada colaborador:
    * Criação de uma nova consulta *Employee x Manager* com os dados dos colaboradores e seu respectivo gerente;
    * Excluída a linha do colaborador James E Borg pois ele não tem gerente;
    * Exclusão das colunas desnecessárias desta nova tabela, mantendo apenas os dados de nome do colaborador e gerente.

* Agrupamento dos dados da tabela *Employee x Manager* para identificar quantos colaboradores cada gerente possui.

* Mescla das tabelas *Departament* e *Dept_locations*:
    * Criação de uma nova consulta *Dept x Location* com os dados dos departamentos e sua respectiva localização;
    * Mescla das colunas de localização e nome do departamento;
    * Exclusão das colunas desnecessárias desta nova tabela, mantendo apenas os dados de localização-nome do departamento e número do departamento.

* Mescla das tabelas *Works_on*, *Company project* e *Company Employee*:
    * Criação de uma nova consulta *Projetos* com os dados de nome do projeto, horas, localização, departamento e colaborador;
     * Exclusão das colunas desnecessárias desta nova tabela.
    
