
FarmTech Solutions - Modelagem de Banco de Dados

Este repositório contém a modelagem de dados relacional da solução proposta pela startup fictícia **FarmTech Solutions**, focada em Agricultura Digital.

Objetivo

Armazenar e analisar os dados coletados por sensores em plantações para otimizar a aplicação de água e nutrientes, além de prever necessidades futuras com base em dados históricos.

Estrutura do Banco de Dados

A modelagem foi realizada no **Oracle SQL Developer Data Modeler** e inclui as seguintes entidades:

| Tabela           | Descrição                                                                 |
|------------------|---------------------------------------------------------------------------|
| `LOCAL`          | Armazena os locais de instalação dos sensores                             |
| `TIPO_SENSOR`    | Tipos de sensores utilizados (umidade, pH, NPK, etc)                      |
| `TIPO_APLICACAO` | Tipos de aplicação realizadas (água, nutrientes, etc)                     |
| `SENSOR`         | Sensores instalados, vinculados ao local e ao tipo de sensor              |
| `CULTURA`        | Informações das culturas monitoradas (tipo de solo, nome, ciclo)          |
| `LEITURA_SENSOR` | Leitura de dados realizada pelos sensores (valor, data/hora, cultura)     |
| `APLICACAO`      | Aplicações realizadas (tipo, quantidade, data/hora, cultura)              |

Relacionamentos

- Um `LOCAL` pode ter muitos `SENSOR`
- Um `TIPO_SENSOR` pode estar ligado a muitos `SENSOR`
- Um `TIPO_APLICACAO` pode estar ligado a muitas `APLICACAO`
- Um `SENSOR` pode gerar muitas `LEITURA_SENSOR`
- Uma `CULTURA` pode ter muitas `LEITURA_SENSOR` e `APLICACAO`

Tecnologias

- Oracle SQL Developer Data Modeler 24.x
- Oracle SQL Developer para execução dos scripts
- Linguagem SQL padrão Oracle (com `NUMBER`, `VARCHAR2`, `TIMESTAMP`)

Arquivos incluídos

- `tabelas.sql`: Script para criar todas as tabelas no Oracle
- `inserts.sql`: Script para criar dados nas tabelas
- `mapaTesouro.docx`: Documento contendo o MER
- `mapaTesouro.png`: Imagem do DER visual com relacionamentos e cardinalidades
- `arquivo.dmd`: Arquivo de projeto do SQL Developer Data Modeler


