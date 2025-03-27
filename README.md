# Guia de Automação de Documentos com Avvoka e Word

## 🎯 Introdução
ATENTAR-SE A DETALHES PEQUENOS, ERROS E DIFERENÇAS

---

## ✅ Etapas do Processo

### 📌 Etapas Iniciais
1. Leitura crítica do documento enviado pelo cliente
2. Formatação do documento antes de subir para Avvoka
3. Subir o arquivo formatado
4. Testar a formatação
5. Corrigir a formatação

### 🚀 Automação no Avvoka
6. Fazer Automação
7. Testar a automação
8. Corrigir pequenos erros
9. Configurar APIs (opcional)
10. Publicar o documento

---

## ✅ Configuração no Word

### 🎯 Criação de Estilos
- Alinhamento
- Numeração
- Criar Estilo padrão (sem negrito ou itálico)
- Uso do TAB para mudar o nível da numeração
- Nome dos estilos com padrão `Adoc_Corpo`, `Adoc_Recuo`, `Adoc_Numeracao`, `Adoc_Citacao`, etc.

---

## ✅ Regras de Automação no Avvoka
- # **Não mexer na automação após exportar o DOCX.**
### ⚙️ Boas práticas

- **Atentar-se aos espaços entre vírgulas** (não colocar vírgulas dentro de variáveis).
- Criar variáveis no padrão `SNAKE_CASE` e sem acentos.
- Variáveis padrão como `POLO_ATIVO`, `POLO_PASSIVO`, `DATA_DOC` e `NUM_VAR`.
- Para criar um bloco vazio, usar um ponto final `.` pintado da cor de fundo do documento.
- Seção
- ##CAIXA ALTA

- Texto explicativo azul(226ce0), negrito e em CAIXA ALTA

- Itálico nas caixas de seleção

- Gênero = condicionar colocando variaveis de masculino e feminino, Nacionalidade ser uma lista aberta

- Estados Civis: Casado, Solteiro, Divorciado, Separado e Viúvo

- Colocar como DICA (Não utilize vírgulas. Separe os reais dos centavos utilizando um ponto. Ex.: 1500.99)

- Quando uma variáveis chegar aos 180 usos, criar uma operação para utilizar mais vezes

- Selecionar Variável colocando um ~ + ESPAÇO (para linkar uma variável a outra)

- **AO MEXER EM MODELOS, NÃO CLIQUE EM "UNPUBLISH". PRIMEIRO, SALVE AS ALTERAÇÕES E, EM SEGUIDA, DESPUBLIQUE E PUBLIQUE NA SEQUÊNCIA.**
    - Isso evita que o cliente fique sem acesso ao modelo.

- Apagar os documentos gerados na aba "Meus documentos" na Avvoka ao final do dia.

- Em caso de valores de R$ não for obrigado ter valores por extenso criar uma operação: OP_ATRIBUTOS>Concatenar>(dentro colocar as API's por extenso), é obrigatório colocar o API_VALOR_XXXXXX_BRL_EXT, mas haverá casos em que não será pedido para aparecer no documento.

- Colocar comentário no último Save do que foi feito ou aleterado (commit).

- Por padrão os valores serão sempre em MINÚSCULO, com exceção do Yes e No e siglas de estado, em botões de rádio, caixas de seleção, etc... Em casos de sigla de estado também é possível criar uma operação>maiúscula>atributo

## ✅ Operações e Loops no Avvoka

 Nome das variaveis das operações começam com OP_XXXX_XXX

### 🔄 Uso de Loops
- Permite repetir elementos dinamicamente, como listas de partes contratantes ou serviços.
- Exemplo de loop: [Clique aqui](#3-operações-e-loops)

### 🔗 Tipos de API suportadas
# Integrações com APIs no Avvoka

## ✅ RECEITA FEDERAL

### Pessoa Física
> **IRF_XXXXXX_CPF**
- IRF_XXXXXX_NOME
- IRF_XXXXXX_NASCIMENTO _(Não é padrão)_

### Pessoa Jurídica
> **IRF_XXXXXX_CNPJ**
- IRF_XXXXXX_RAZAO_SOCIAL
- IRF_XXXXXX_ENDERECO
- IRF_XXXXXX_NUM_ENDERECO
- IRF_XXXXXX_COMPLEMENTO _(Opcional)_
- IRF_XXXXXX_BAIRRO
- IRF_XXXXXX_CIDADE
- IRF_XXXXXX_ESTADO
- IRF_XXXXXX_CEP
- IRF_XXXXXX_NOME_FANTASIA _(Não é padrão)_
- IRF_XXXXXX_NATUREZA _(Não é padrão)_

---

## ✅ CORREIOS

> **ICEP_XXXXXX_CEP**
- ICEP_XXXXXX_ENDERECO
- ICEP_XXXXXX_COMPLEMENTO _(Oculta)_
- ICEP_XXXXXX_BAIRRO
- ICEP_XXXXXX_CIDADE
- ICEP_XXXXXX_ESTADO

---

## ✅ VALOR POR EXTENSO

> **API_VALOR_XXXXXX_BRL**
- API_VALOR_XXXXXX_BRL_EXT

**Exemplo de uso:**
> O valor da causa é de **API_VALOR_CAUSA_BRL** (**API_VALOR_CAUSA_BRL_EXT**).

---

## ✅ Outras Integrações pouco usadas
- LOY
- JUDICE
- ILEX

---

## 🎯 Observações Importantes
- Sempre que as variáveis estiverem fora do padrão, precisamos ser informados.
- Todas as partes do documento precisam conter as mesmas variáveis.
- Não utilize vírgulas. Separe os reais dos centavos utilizando um ponto. Ex.: 1500.99

---

## ✅ Códigos para Formatação de Datas (Avvoka)
| Código | Exemplo       | Descrição                      |
|---------|----------------|----------------------------------|
| `%d`       | 15                   | Dia do mês (01-31)            |
| `%B`      | março             | Nome completo do mês     |
| `%b`      | mar                 | Nome do mês abreviado |
| `%m`      | 03                   | Mês em números (01-12) |
| `%Y`      | 2025               | Ano com 4 dígitos             |
| `%y`      | 25                    | Ano com 2 dígitos              |
| `%A`      | sexta-feira     | Dia da semana por extenso |
| `%a`      | sex                  | Dia da semana abreviado |
| `%H`      | 14                    | Hora (00-23)                      |
| `%I`        | 02                    | Hora (01-12, formato 12h) |
| `%p`       | PM                  | AM ou PM                              |
| `%M`     | 45                    | Minutos (00-59)                    |
| `%S`      | 30                    | Segundos (00-59)                  |
| `%Z`      | GMT-3             | Fuso horário                            |
| `%j`        | 074                  | Dia do ano (001-365)             |
| `%w`      | 5                      | Dia da semana (0=domingo, 6=sábado) |

---

## ✅ Espaços para imagens explicativas

# 1. Processo de formatação no Word
![Word](/imgs/1.png)
### PASSO 1: Criar estilos para padronizar o documento.
### PASSO 2: Tabela de numeração para número de tópicos e cláusulas.
---
![Word](/imgs/2.png)
### PASSO 3: Selecionar o tipo de numeração.
---
![Word](/imgs/3.png)
### PASSO 4: Definir o nível dos parágrafos.
### PASSO 5: Tipos de níveis prontos e exemplos.
### PASSO 6: Para configurar o nível manualmente.
### OBS 1: Estilos, como cores da fonte, negrito, itálico, etc.
---
![Word](/imgs/4.png)
### PASSO 7: Tela de configuração dos níveis.
---
![Word](/imgs/5.png)
### OBS 2: Lista de comentários a ser seguido para a automação, e o que o cliente deseja.
---
![Word](/imgs/6.png)
### OBS 3: Tela para mostrar estilos utilizados.
--- 
---
# 2. Automação Avvoka 
![Automação Avvoka](/imgs/7.png)
### OBS 1: Opção Início para alterar alguma fonte ou colocar diretamente estilos pela Avvoka.
---
![Automação Avvoka](/imgs/8.png)
### OBS 2: Opção Inserir possibilita colocar e criar tabelas.
---
![Automação Avvoka](/imgs/9.png)
### OBS 3: Opção Estilos possibilita ver os estilos que foram aplicados do Word.
---
![Automação Avvoka](/imgs/10.png)
### OBS 4: Opção Automação é onde criamos as variáveis, condicionais, loops e colocamos as operações.
---
![Automação Avvoka](/imgs/11.png)
### OBS 5: Cria a variável.
---
![Automação Avvoka](/imgs/12.png)
### OBS 6: Insere condição de linha.
---
![Automação Avvoka](/imgs/13.png)
### OBS 7: Insere condição de bloco.
---
## 3. Operações e Loops
![Operações e Loops](/imgs/14.png)
### OBS 8: Cria o loop. 
---
![Operações e Loops](/imgs/15.png)
### OBS 8.1: Aqui inserimos o nome do loop.
---
![Operações e Loops](/imgs/16.png)
### OBS 8.2: Em caso de loop escravo, aqui escolhemos o loop mestre pelo nome de outro loop.
---
![Operações e Loops](/imgs/17.png)
### OBS 8.3: Muda o nome do controlador do repetidor, onde muda o nome do botão para "acrescentar" algo no loop.
---
![Operações e Loops](/imgs/18.png)
### OBS 9: Inserir operação.
---
![Operações e Loops](/imgs/19.png)
### OBS 10: Lista onde ficam as operações criadas.
---
![Operações e Loops](/imgs/20.png)
### OBS 10.1: Exemplo de operação para formatar valor em dinheiro.
---
![Operações e Loops](/imgs/21.png)
### OBS 10.2: Exemplo de operação com Regex, para modificar uma palavra para encaixar em uma frase de forma coesa.
---
![Operações e Loops](/imgs/22.png)
### OBS 10.3: Continuação da OBS 10.3.
---
![Operações e Loops](/imgs/23.png)
### OBS 10.4: Criamos operações assim em casos da variável estar próxima dos 180 usos.
---
![Operações e Loops](/imgs/24.png)
### OBS 10.5: Criamos operações assim em casos da variável estar próxima dos 180 usos.
---
![Operações e Loops](/imgs/25.png)
### OBS 10.6: Exemplo de operação para formatar valor em dinheiro.
---
![Operações e Loops](/imgs/26.png)
### OBS 10.7: Exemplo de operação para formatar o tipo data.
---
![Operações e Loops](/imgs/27.png)
### OBS 10.8: Operação para pegar a data do sistema e utilizar a data atual do computador.
---
![Operações e Loops](/imgs/28.png)
### OBS 10.9: Operação para concatenar algo e fazer um conjunto, fazendo por exemplo uma lista.
---
![Operações e Loops](/imgs/29.png)
### OBS 10.10: Operação para contar quantos elementos possui na lista.
---
![Operações e Loops](/imgs/30.png)
### OBS 10.11: Exemplo de operação para flexão de gênero.
---
![Operações e Loops](/imgs/31.png)
### OBS 10.11.1: Continuação do exemplo - flexão de gênenro.
---
![Operações e Loops](/imgs/32.png)
### OBS 10.11.2: Continuação do exemplo - flexão de gênenro.
---
![Operações e Loops](/imgs/33.png)
### OBS 10.11.3: Continuação do exemplo - flexão de gênenro.
---
![Operações e Loops](/imgs/34.png)
### OBS 10.11.4: Continuação do exemplo - flexão de gênenro.
---
![Operações e Loops](/imgs/35.png)
### OBS 10.11.5: Continuação do exemplo - flexão de gênenro.
---
![Operações e Loops](/imgs/36.png)
### OBS 10.12: Exemplo de operação de loop em linha.
---
![Operações e Loops](/imgs/37.png)
### OBS 10.12.1: Continuação do exemplo de operação de loop em linha.
---
![Operações e Loops](/imgs/38.png)
### OBS 10.12.2: Continuação do exemplo de operação de loop em linha.
---
![Operações e Loops](/imgs/47.png)
### OBS 10.13: Para linkar uma variável a outra aperte ~ + ESPAÇO para fazer essa conexão.
---
![Operações e Loops](/imgs/48-modified.png)
### OBS 10.14: Exemplo de operação de soma onde começa em 1 e vai adicionando +1 conforme aumenta o loop.
---
# 4. Exemplo de questionário no Avvoka
![Questionário](/imgs/39.png)
### OBS 11: Caixa de Seções criadas, as quais têm um fundo azul claro.
### OBS 12: Perguntas do questionário, onde possuir [AUTO] é preenchido automaticamente.
---
![Questionário](/imgs/40.png)
### OBS 13: Opções de tipos de questionários podendo ser, texto, número, do tipo data, botões, etc.
---
![Questionário](/imgs/41.png)
### OBS 14: Outras opções como listas. 
---
![Questionário](/imgs/42.png)
### OBS 15: Aqui conseguimos ver a quantidade de vezes que foi utilizado uma variável, onde foi utilizada e alterar o nome da mesma.
---
![Questionário](/imgs/43.png)
### OBS 16: No Histórico conseguimos ver os SAVES anteriores.
---
![Questionário](/imgs/44.png)
### OBS 17: Aqui configuramos o título do documento gerado de forma dinâmica.
---

# 5. Configuração de API
![Configuração da API](/imgs/45.png)
### OBS 18: Aqui configuramos as API's que vão ser usadas, por padrão **IRF_XXXXXX_CPF**, **IRF_XXXXXX_CNPJ**, **ICEP_XXXXXX_CEP** e **API_VALOR_XXXXXX_BRL**.

---

## 🚀 Conclusão
Seguindo este guia, é possível automatizar contratos, configurar variáveis, integrar APIs e personalizar documentos com eficiência na plataforma Avvoka.
