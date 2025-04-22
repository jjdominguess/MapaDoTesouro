# FIAP - Faculdade de Informática e Administração Paulista 

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

# Nome do projeto
  Mapa do Tesouro - Fase 2
## 👨‍🎓 Integrantes: 
- <a>João José Domingues Silva</a>
- <a>Lais Londo Claus</a>
- <a>Murilo Santana</a> 
- <a>Lucas Alves Ladeira</a> 
- <a>Carlos Eduardo Campos Lanzi</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/company/inova-fusca">Lucas Gomes Moreira</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/company/inova-fusca">Nome do Coordenador</a>

## 📜 Descrição

O objetivo é criar um sistema de banco de dados relacional para armazenar e analisar dados coletados por sensores em plantações, a fim de otimizar o uso de recursos como água e nutrientes.


<b> Exemplo de perguntas que o modelo responde </b> <br>

<b>- Quais leituras de sensores foram realizadas para uma determinada cultura? </b> <br>

(Relacionamento entre LeituraSensor e Cultura) <br> <br>

<b>- Qual foi o valor da leitura de um sensor em um determinado período? </b> <br>

(Filtro por data_hora e sensor_id na tabela LeituraSensor) <br><br>

<b>- Qual a média de leitura de um sensor específico durante o ciclo da cultura? </b> <br>

(Junta LeituraSensor, Sensor e Cultura para análise por período) <br><br>

<b>- Quais sensores estão instalados em determinado local? </b> <br>

(Relacionamento entre Sensor e Local) <br><br>


   <b>Entidades e Atributos (Modelo Entidade-Relacionamento - MER) </b> <br><br>
    • Sensor <br>
      - sensor_id (PK) <br>
      - tipo_sensor_id (FK) <br>
      - local_id (FK) <br><br>
    • Cultura <br>
      - cultura_id (PK) <br>
      - nome_cultura <br>
      - tipo_solo <br>
      - ciclo_dias <br><br>
    • LeituraSensor <br>
      - leitura_id (PK) <br>
      - data_hora <br>
      - valor <br>
      - sensor_id (FK) <br>
      - cultura_id (FK) <br><br>
    • Aplicacao <br>
      - aplicacao_id (PK) <br>
      - data_hora <br>
      - tipo_aplicacao_id (FK) <br>
      - quantidade <br>
      - cultura_id (FK) <br><br>
    • Local <br>
      - local_id (PK) <br>
      - descricao_local <br><br>
    • TipoSensor <br>
      - tipo_sensor_id (PK) <br>
      - descricao_tipo <br><br>
    • TipoAplicacao <br>
      - tipo_aplicacao_id (PK) <br>
      - descricao_aplicacao <br> <br>

<b>Cardinalidade dos Relacionamentos </b> <br>
    •	Sensor → TipoSensor = N:1 <br>
    •	Sensor → Local = N:1 <br>
    •	Sensor → LeituraSensor = 1:N <br>
    •	Cultura → LeituraSensor = 1:N <br>
    •	Cultura → Aplicacao = 1:N <br>
    •	Aplicacao → TipoAplicacao = N:1 <br><br>

<b>Tipos de Dados por Atributo </b><br><br>
   • sensor_id: INTEGER <br>
   • tipo_sensor_id: INTEGER <br>
   • local_id: INTEGER <br>
   • cultura_id: INTEGER <br>
   • nome_cultura: VARCHAR(50) <br>
   • tipo_solo: VARCHAR(30) <br>
   • ciclo_dias: INTEGER <br>
   • leitura_id: INTEGER <br>
   • data_hora: DATETIME <br>
   • valor: DOUBLE <br>
   • aplicacao_id: INTEGER <br>
   • tipo_aplicacao_id: INTEGER <br>
   • quantidade: DOUBLE <br>
   • descricao_local: VARCHAR(100) <br>
   • descricao_tipo: VARCHAR(20) <br>
   • descricao_aplicacao: VARCHAR(20) <br>




  
## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:


- <b>arquivo.dmd - Exportado do Oracle Data Modeler</b>: 

- <b>mapaTesouro.png - Imagem gráfica da modelagem</b>: 

- <b>mapaTesouro.docx - Arquivo contendo o MER</b>: 

- <b>tabelas.sql - Script SQL para criação das tabelas</b>:

- <b>inserts.sql - Script SQL para inclusão de dados fictícios nas tabelas</b>: 

- <b>README.md</b>: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).


## 🗃 Histórico de lançamentos

* 1.0.0 - 22/04/2025

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
