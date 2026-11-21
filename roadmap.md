# 🗺️ Roadmap — CorreAki 2027

> **Origem**: template de roadmap da dinâmica D² ([roadmap.jpeg](roadmap.jpeg)) + ondas de [ondas.md](ondas.md)
> **Imagem**: [roadmap-correaki.png](roadmap-correaki.png)
> **Status**: proposta. As estimativas precisam ser validadas pelo Líder Técnico (regra 3).

## Regras

1. Uma onda não pode ultrapassar 3 meses.
2. As ondas são sequenciais.
3. A definição da duração das ondas deve ser estimada no roadmap pelo Líder Técnico (considerando composição do time, senioridade e maturidade).

## Time

- **5 devs plenos**
- **1 estagiário**: apoia testes, ajustes de interface e tasks pequenas, sem ser contado na capacidade.

## Como estimamos

**Por task** (1 dev pleno):

| Esforço (aba Confiança) | Semanas |
|:---:|:---:|
| 1 E | 1 |
| 2 E | 2 |
| 3 E | 3 |

Ajustes:
- **+1 semana** para task com confiança **Baixa** 🟥.
- **+1 semana** para task com **integração externa** (meios de pagamento).
- **−1 semana** para task de 3 semanas ou mais, que recebe **2 devs** (o time de 5 permite).

**Por onda**: as tasks rodam em paralelo (no máximo 3 tasks e 5 devs por onda). A onda dura a **task mais longa + 1 semana de testes e homologação**. Feriados não foram descontados.

---

## Visão geral

| | **Q1** | | | **Q2** | | | **Q3** | | | **Q4** | | |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **Mês** | JAN | FEV | MAR | ABR | MAI | JUN | JUL | AGO | SET | OUT | NOV | DEZ |
| **Ondas** | 1 · 2 | 2 · 3 | 3 · 4 | 4 · 5 · 6 | 6 · 7 | 7 · 8 | 8 · 9 · 10 | 10 · 11 | 11 · 12 | | | |

| Onda | Período | Duração |
|:---:|---|:---:|
| 1 | 04/01 a 22/01 | 3 semanas |
| 2 | 25/01 a 12/02 | 3 semanas |
| 3 | 15/02 a 05/03 | 3 semanas |
| 4 | 08/03 a 02/04 | 4 semanas |
| 5 | 05/04 a 23/04 | 3 semanas |
| 6 | 26/04 a 21/05 | 4 semanas |
| 7 | 24/05 a 11/06 | 3 semanas |
| 8 | 14/06 a 02/07 | 3 semanas |
| 9 | 05/07 a 23/07 | 3 semanas |
| 10 | 26/07 a 13/08 | 3 semanas |
| 11 | 16/08 a 03/09 | 3 semanas |
| 12 | 06/09 a 24/09 | 3 semanas |
| | **Total** | **38 semanas** |

Nenhuma onda passa de 3 meses (regra 1). Todas as features terminam em setembro e o Q4 fica livre.

---

## Detalhe por onda

### Onda 1 · 04/01 a 22/01 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Criação de usuário e senha | 1 | 🟩 | | 1 | 1 sem |
| Filtros de local, data e distância | 2 | 🟨 | | 1 | 2 sem |
| LGPD | 1 | 🟩 | | 1 | 1 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 2 · 25/01 a 12/02 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Filtro de texto | 1 | 🟨 | | 1 | 1 sem |
| Área de detalhes da prova | 2 | 🟥 | +1 confiança baixa, −1 dois devs | 2 | 2 sem |
| Esqueci senha | 1 | 🟩 | | 1 | 1 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 3 · 15/02 a 05/03 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Dados de local de entrega ou retirada | 2 | 🟥 | +1 confiança baixa, −1 dois devs | 2 | 2 sem |
| Dados de pagamento | 3 | 🟩 | −1 dois devs | 2 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 4 · 08/03 a 02/04 (4 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Integrações com meios de pagamento | 3 | 🟩 | +1 integração, −1 dois devs | 2 | 3 sem |
| Objetivos no esporte | 1 | 🟩 | | 1 | 1 sem |
| Logout | 1 | 🟩 | | 1 | 1 sem |
| | | | **Mais longa 3 + testes 1** | | **4 sem** |

### Onda 5 · 05/04 a 23/04 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Validação de dados de pagamento | 3 | 🟩 | −1 dois devs | 2 | 2 sem |
| Parametrização PCD | 1 | 🟥 | +1 confiança baixa | 1 | 2 sem |
| Termos de uso | 1 | 🟨 | | 1 | 1 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 6 · 26/04 a 21/05 (4 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Valor de frete | 3 | 🟥 | +1 confiança baixa, −1 dois devs | 2 | 3 sem |
| Cancelar conta | 2 | 🟩 | | 1 | 2 sem |
| | | | **Mais longa 3 + testes 1** | | **4 sem** |

### Onda 7 · 24/05 a 11/06 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Aplicação de descontos | 3 | 🟨 | −1 dois devs | 2 | 2 sem |
| Dados pessoais | 2 | 🟩 | | 1 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 8 · 14/06 a 02/07 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Histórico da jornada da corrida inscrita | 3 | 🟩 | −1 dois devs | 2 | 2 sem |
| Transferência de titularidade | 2 | 🟨 | | 1 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 9 · 05/07 a 23/07 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Histórico de corridas | 3 | 🟩 | −1 dois devs | 2 | 2 sem |
| Avisos com informações da prova | 2 | 🟩 | | 1 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 10 · 26/07 a 13/08 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Cancelamento de inscrição | 1 | 🟥 | +1 confiança baixa | 1 | 2 sem |
| Alertas de compra | 2 | 🟩 | | 1 | 2 sem |
| Alertas de alteração de cadastro | 2 | 🟩 | | 1 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 11 · 16/08 a 03/09 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Alertas de entrega | 2 | 🟩 | | 1 | 2 sem |
| Pontuação e ranking | 2 | 🟥 | +1 confiança baixa, −1 dois devs | 2 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

### Onda 12 · 06/09 a 24/09 (3 semanas)
| Task | E | Confiança | Ajuste | Devs | Estimativa |
|---|:---:|:---:|---|:---:|:---:|
| Alerta de cancelamento | 2 | 🟩 | | 1 | 2 sem |
| Configuração de alertas | 2 | 🟩 | | 1 | 2 sem |
| | | | **Mais longa 2 + testes 1** | | **3 sem** |

---

## Marcos

| Data | Marco |
|---|---|
| **12/02** | Busca e detalhes das corridas prontos (fim da Onda 2) |
| **23/04** | Inscrição paga funcionando de ponta a ponta (fim da Onda 5) |
| **21/05** | Frete calculado no checkout (fim da Onda 6) |
| **02/07** | Acompanhamento do kit no app (fim da Onda 8) |
| **24/09** | Todas as features do one-pager entregues (fim da Onda 12) |

---

## Pontos para o grupo revisar

1. **Estimativas iniciais**: o Líder Técnico precisa revisar a regra de semanas por esforço e os ajustes.
2. **Capacidade sobrando**: nas ondas com 2 tasks, 1 ou 2 devs ficam livres. Eles podem cuidar de bugs, dívida técnica e da preparação da onda seguinte (discovery das tasks com confiança baixa).
3. **Q4 livre**: com 38 semanas, tudo termina em setembro. O Q4 pode receber melhorias vindas do teste de usabilidade ([validacao.md](validacao.md)) ou novas features.
4. **Cancelamento de inscrição só em agosto**: quem se inscrever a partir de abril fica cerca de 4 meses sem conseguir cancelar pelo app.
