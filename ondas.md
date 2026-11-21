# 🌊 Sequenciador de Ondas — CorreAki

> **Origem**: quadro de ondas da dinâmica D² ([ONDAS.jpeg](ONDAS.jpeg)) + aba **Confiança** da planilha de features
> **Status**: proposta para o grupo validar.

## Como ler

- **Cor do cartão** = coluna **RESULTADO** da aba Confiança: 🟩 Alta · 🟨 Média · 🟥 Baixa
- **E** = esforço · **$** = valor para o negócio · **S2** = valor para UX (de 1 a 3)

## Regras

1. Uma onda pode conter no máximo 3 cartões.
2. Uma onda não pode ter mais de um cartão vermelho.
3. Uma onda não pode ter três cartões somente amarelos ou vermelhos.
4. A soma de esforço não pode ultrapassar 5 E's.
5. A soma de valor não pode ser menor que quatro $'s e quatro S2's.
6. Se um cartão depende de outro, deve estar em uma onda anterior.

---

## Visão geral

| Onda | Cartões | E | $ | S2 |
|---|---|:---:|:---:|:---:|
| **1** | 🟩 Criação de usuário e senha · 🟨 Filtros de local, data e distância · 🟩 LGPD | 4 | 5 | 6 |
| **2** | 🟨 Filtro de texto · 🟥 Área de detalhes da prova · 🟩 Esqueci senha | 4 | 5 | 7 |
| **3** | 🟥 Dados de local de entrega ou retirada · 🟩 Dados de pagamento | 5 | 5 | 6 |
| **4** | 🟩 Integrações com meios de pagamento · 🟩 Objetivos no esporte · 🟩 Logout | 5 | 5 | 5 |
| **5** | 🟩 Validação de dados de pagamento · 🟥 Parametrização PCD · 🟨 Termos de uso | 5 | 6 | 5 |
| **6** | 🟥 Valor de frete · 🟩 Cancelar conta | 5 | 4 | 6 |
| **7** | 🟨 Aplicação de descontos · 🟩 Dados pessoais | 5 | 4 | 4 |
| **8** | 🟩 Histórico da jornada da corrida inscrita · 🟨 Transferência de titularidade | 5 | 6 | 6 |
| **9** | 🟩 Histórico de corridas · 🟩 Avisos com informações da prova | 5 | 4 | 6 |
| **10** | 🟥 Cancelamento de inscrição · 🟩 Alertas de compra · 🟩 Alertas de alteração de cadastro | 5 | 7 | 8 |
| **11** | 🟩 Alertas de entrega · 🟥 Pontuação e ranking | 4 | 5 | 6 |
| **12** | 🟩 Alerta de cancelamento · 🟩 Configuração de alertas | 4 | 5 | 6 |

**Total**: 29 cartões em 12 ondas. Todas as ondas respeitam as 6 regras.

---

## Detalhe por onda

### Onda 1
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Criação de usuário e senha | Acesso | 🟩 Alta | 1 | 1 | 1 |
| Filtros de local, data e distância *(post-it "Busca de corrida")* | Calendário e buscas | 🟨 Média | 2 | 3 | 3 |
| LGPD | Legal | 🟩 Alta | 1 | 1 | 2 |
| **Total** | | | **4** | **5** | **6** |

### Onda 2
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Filtro de texto | Calendário e buscas | 🟨 Média | 1 | 2 | 3 |
| Área de detalhes da prova | Calendário e buscas | 🟥 Baixa | 2 | 2 | 3 |
| Esqueci senha | Acesso | 🟩 Alta | 1 | 1 | 1 |
| **Total** | | | **4** | **5** | **7** |

### Onda 3
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Dados de local de entrega ou retirada | Inscrições | 🟥 Baixa | 2 | 2 | 3 |
| Dados de pagamento | Checkout | 🟩 Alta | 3 | 3 | 3 |
| **Total** | | | **5** | **5** | **6** |

### Onda 4
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Integrações com meios de pagamento | Checkout | 🟩 Alta | 3 | 3 | 1 |
| Objetivos no esporte | Perfil | 🟩 Alta | 1 | 1 | 3 |
| Logout | Acesso | 🟩 Alta | 1 | 1 | 1 |
| **Total** | | | **5** | **5** | **5** |

### Onda 5
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Validação de dados de pagamento | Checkout | 🟩 Alta | 3 | 3 | 1 |
| Parametrização PCD | Perfil | 🟥 Baixa | 1 | 2 | 3 |
| Termos de uso | Legal | 🟨 Média | 1 | 1 | 1 |
| **Total** | | | **5** | **6** | **5** |

### Onda 6
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Valor de frete | Checkout | 🟥 Baixa | 3 | 3 | 3 |
| Cancelar conta | Perfil | 🟩 Alta | 2 | 1 | 3 |
| **Total** | | | **5** | **4** | **6** |

### Onda 7
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Aplicação de descontos | Checkout | 🟨 Média | 3 | 3 | 3 |
| Dados pessoais | Perfil | 🟩 Alta | 2 | 1 | 1 |
| **Total** | | | **5** | **4** | **4** |

### Onda 8
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Histórico da jornada da corrida inscrita | Inscrições | 🟩 Alta | 3 | 3 | 3 |
| Transferência de titularidade | Inscrições | 🟨 Média | 2 | 3 | 3 |
| **Total** | | | **5** | **6** | **6** |

### Onda 9
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Histórico de corridas | Perfil | 🟩 Alta | 3 | 2 | 3 |
| Avisos com informações da prova | Notificações | 🟩 Alta | 2 | 2 | 3 |
| **Total** | | | **5** | **4** | **6** |

### Onda 10
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Cancelamento de inscrição | Inscrições | 🟥 Baixa | 1 | 2 | 2 |
| Alertas de compra | Notificações | 🟩 Alta | 2 | 3 | 3 |
| Alertas de alteração de cadastro | Notificações | 🟩 Alta | 2 | 2 | 3 |
| **Total** | | | **5** | **7** | **8** |

### Onda 11
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Alertas de entrega | Notificações | 🟩 Alta | 2 | 3 | 3 |
| Pontuação e ranking | Perfil | 🟥 Baixa | 2 | 2 | 3 |
| **Total** | | | **4** | **5** | **6** |

### Onda 12
| Cartão | Grupo | Confiança | E | $ | S2 |
|---|---|:---:|:---:|:---:|:---:|
| Alerta de cancelamento | Notificações | 🟩 Alta | 2 | 3 | 3 |
| Configuração de alertas | Notificações | 🟩 Alta | 2 | 2 | 3 |
| **Total** | | | **4** | **5** | **6** |

---

## Dependências consideradas (regra 6)

As dependências não estão na planilha; foram inferidas pela lógica do produto.

| Cartão | Depende de | Ondas |
|---|---|---|
| Esqueci senha, Logout, Objetivos, PCD, Cancelar conta | Criação de usuário e senha | 1 → 2, 4, 5, 6 |
| Área de detalhes da prova | Filtros de busca | 1 → 2 |
| Dados de entrega ou retirada | Área de detalhes da prova | 2 → 3 |
| Integrações com meios de pagamento | Dados de pagamento | 3 → 4 |
| Validação de dados de pagamento | Dados de pagamento e integrações | 3, 4 → 5 |
| Valor de frete | Dados de entrega ou retirada | 3 → 6 |
| Aplicação de descontos | Dados de pagamento | 3 → 7 |
| Histórico da jornada, Transferência | Checkout completo | 5 → 8 |
| Histórico de corridas, Avisos da prova | Checkout completo | 5 → 9 |
| Cancelamento de inscrição, Alertas de compra | Checkout completo | 5 → 10 |
| Alertas de alteração de cadastro | Dados pessoais | 7 → 10 |
| Alertas de entrega | Histórico da jornada | 8 → 11 |
| Pontuação e ranking | Histórico de corridas | 9 → 11 |
| Alerta de cancelamento | Cancelamento de inscrição | 10 → 12 |
| Configuração de alertas | Alertas existentes | 10, 11 → 12 |

---

## Pontos para o grupo revisar

1. **Coluna K da planilha**: marca Criação de usuário, Esqueci senha, Logout, Termos de uso e LGPD como Onda 1. São 5 cartões, o que quebra a regra 1, por isso foram distribuídos entre as ondas 1, 2, 4 e 5.
2. **"Busca de corrida"** (post-it da Onda 1) foi tratada como o cartão "Filtros de local, data e distância".
3. **Termos de uso na Onda 5**: dá para trocar de lugar com LGPD (Onda 1) sem quebrar nenhuma regra, se o grupo preferir os termos junto com o cadastro.
4. **Checkout completo só na Onda 5**: a inscrição paga só fecha depois de dados de pagamento, integrações e validação. Como cada um tem esforço 3, não cabem juntos na mesma onda.
