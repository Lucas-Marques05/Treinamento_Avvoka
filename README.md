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

## ✅ Operações e Loops no Avvoka

 Nome das variaveis das operações começam com OP_XXXX_XXX

### 🔄 Uso de Loops
- Permite repetir elementos dinamicamente, como listas de partes contratantes ou serviços.
- Exemplo de loop: [Clique aqui](#4-operações-e-loops)

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

### 1. Processo de formatação no Word

### 2. Automação Avvoka 

### 3. Exemplo de questionário no Avvoka

### 4. Operações e Loops

### 5. Configuração de API

---

## 🚀 Conclusão
Seguindo este guia, é possível automatizar contratos, configurar variáveis, integrar APIs e personalizar documentos com eficiência na plataforma Avvoka.
