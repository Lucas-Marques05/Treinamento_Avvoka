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
- Estilo padrão (sem negrito ou itálico)
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

## 1. Processo de formatação no Word
![Word](/imgs/1.png)
![Word](/imgs/2.png)
![Word](/imgs/3.png)
![Word](/imgs/4.png)
![Word](/imgs/5.png)
![Word](/imgs/6.png)

## 2. Automação Avvoka 
![Automação Avvoka](/imgs/7.png)
![Automação Avvoka](/imgs/8.png)
![Automação Avvoka](/imgs/9.png)
![Automação Avvoka](/imgs/10.png)
![Automação Avvoka](/imgs/11.png)
![Automação Avvoka](/imgs/12.png)
![Automação Avvoka](/imgs/13.png)

## 3. Operações e Loops
![Operações e Loops](/imgs/14.png)
![Operações e Loops](/imgs/15.png)
![Operações e Loops](/imgs/16.png)
![Operações e Loops](/imgs/17.png)
![Operações e Loops](/imgs/18.png)
![Operações e Loops](/imgs/19.png)
![Operações e Loops](/imgs/20.png)
![Operações e Loops](/imgs/21.png)
![Operações e Loops](/imgs/22.png)
![Operações e Loops](/imgs/23.png)
![Operações e Loops](/imgs/24.png)
![Operações e Loops](/imgs/25.png)
![Operações e Loops](/imgs/26.png)
![Operações e Loops](/imgs/27.png)
![Operações e Loops](/imgs/28.png)
![Operações e Loops](/imgs/29.png)
![Operações e Loops](/imgs/30.png)
![Operações e Loops](/imgs/31.png)
![Operações e Loops](/imgs/32.png)
![Operações e Loops](/imgs/33.png)
![Operações e Loops](/imgs/34.png)
![Operações e Loops](/imgs/35.png)
![Operações e Loops](/imgs/36.png)
![Operações e Loops](/imgs/37.png)
![Operações e Loops](/imgs/38.png)

## 4. Exemplo de questionário no Avvoka
![Questionário](/imgs/39.png)
![Questionário](/imgs/40.png)
![Questionário](/imgs/41.png)
![Questionário](/imgs/42.png)
![Questionário](/imgs/43.png)
![Questionário](/imgs/44.png)

### 5. Configuração de API
![Configuração da API](/imgs/45.png)

---

## 🚀 Conclusão
Seguindo este guia, é possível automatizar contratos, configurar variáveis, integrar APIs e personalizar documentos com eficiência na plataforma Avvoka.
