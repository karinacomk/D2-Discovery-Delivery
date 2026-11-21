# 📊 Métricas HEART — CorreAki

> **Produto**: plataforma B2C, web e app mobile, para corredores de rua encontrarem corridas de vários organizadores, se inscreverem e receberem ou retirarem o kit.
> **Momento**: validação · foco em aquisição, depois retenção.
> **Metas (6 a 12 meses)**: recorrência de 50% em 12 meses · fidelizar pela experiência do kit · jornada de inscrição acessível para corredores PCD.
> **Base das fórmulas**: catálogo de métricas D² ([Lista de Métricas - Product Management.xlsx](materiais/Lista%20de%20M%C3%A9tricas%20-%20Product%20Management.xlsx)).
> **Preview do dashboard**: [dashboard-heart-correaki.png](dashboard-heart-correaki.png) (dados simulados).

---

## Matriz HEART

| Frente HEART | Objetivos | Sinais | Métricas sugeridas |
|---|---|---|---|
| **Happiness, Satisfação** | O corredor se sente seguro e satisfeito ao se inscrever e ao receber o kit sem precisar se deslocar | Avalia bem a entrega do kit; recomenda o CorreAki para amigos e para o grupo de corrida; relata pouco esforço para se inscrever | Customer Satisfaction Score (CSAT) do kit · Net Promoter Score (NPS) · Customer Effort Score (CES) da inscrição |
| **Engagement, Engajamento** | O corredor usa o CorreAki como lugar de referência para encontrar corridas e acompanhar o kit | Volta ao app para buscar provas e usar filtros; consulta o status do kit enquanto espera a entrega | Usuários ativos · Uso de busca interna · Frequência de uso da funcionalidade (acompanhamento do kit) |
| **Adoption, Adoção** | Corredores novos fazem a primeira inscrição e escolhem receber o kit pelo CorreAki | Sai da busca para os detalhes da prova e conclui o pagamento; escolhe "Receber em casa" ou "Ponto parceiro" em vez de retirar no organizador | Taxa de ativação · Taxa de conversão por etapa do funil · % Adoção de funcionalidade (entrega do kit) |
| **Retention, Retenção** | O corredor volta a se inscrever em novas provas pelo CorreAki (meta de 50% em 12 meses) | Faz uma segunda inscrição depois da primeira prova; continua se inscrevendo ao longo do ano | Taxa de retenção · Taxa de churn |
| **Task Success, Sucesso em tarefas** | O corredor conclui a inscrição sem erro, inclusive corredores PCD, e recebe o kit no prazo | Termina o checkout sem desistir; não trava em campos ou validações; o kit chega antes da prova | Taxa de sucesso na tarefa (inscrição) · Taxa de abandono (checkout) · % de kits entregues no prazo *(métrica derivada do contexto)* |

---

## Fórmulas

**Legenda**
- ⚠️ **Proposta a validar**: a planilha traz só uma definição, ou uma fórmula incompleta ou invertida. O cálculo apresentado não é a fórmula literal do Excel.
- *Métrica derivada do contexto*: não consta no catálogo.

### Happiness, Satisfação

#### 1. Customer Satisfaction Score (CSAT) do kit
| | |
|---|---|
| **Cálculo** | `(respostas "satisfeito" + "muito satisfeito" / total de respostas) × 100` |
| **Medição** | Pesquisa de 1 a 5 enviada até 24h depois de o kit ser marcado como entregue ou retirado |
| **Base** | Corredores que receberam o kit no período |
| **Janela** | Mensal |
| **Origem** | `Métricas de Produto!33` (também em `Métricas de UX!24`) |

#### 2. Net Promoter Score (NPS)
| | |
|---|---|
| **Cálculo** | `% de promotores (notas 9 e 10) − % de detratores (notas 0 a 6)`. O resultado vai de −100 a +100 |
| **Medição** | Pergunta "De 0 a 10, quanto você recomendaria o CorreAki?", feita depois da prova |
| **Base** | Corredores com pelo menos 1 prova concluída |
| **Janela** | Trimestral |
| **Origem** | `Métricas de Produto!34` |

#### 3. Customer Effort Score (CES) da inscrição
| | |
|---|---|
| **Cálculo** | `Σ (nota de 1 a 5 × número de respondentes com essa nota) / total de respondentes` |
| **Medição** | Pergunta "Foi fácil concluir sua inscrição?" na tela de confirmação. Escala de 1 (muito difícil) a 5 (muito fácil): quanto maior, melhor |
| **Base** | Inscrições concluídas |
| **Janela** | Mensal |
| **Origem** | `Métricas de UX!25`. A versão de `Métricas de Produto!58` usa emoticons e não tem fórmula, por isso foi usada a de UX |

### Engagement, Engajamento

#### 4. Usuários ativos
| | |
|---|---|
| **Cálculo** | Contagem de corredores únicos com pelo menos 1 evento qualificado no mês (MAU) |
| **Medição** | Evento qualificado = buscar uma corrida, abrir os detalhes de uma prova ou consultar o acompanhamento do kit. Login sozinho não conta |
| **Base** | Todos os corredores cadastrados |
| **Janela** | Mensal |
| **Origem** | `Métricas de Produto!18`. A planilha cita DAU, WAU e MAU, sem divisão. ⚠️ **Proposta de operacionalização**: contagem mensal, porque corredores se inscrevem poucas vezes por mês |

#### 5. Uso de busca interna
| | |
|---|---|
| **Cálculo** | `buscas realizadas no período / usuários ativos no período` |
| **Medição** | Busca = envio de texto ou aplicação de filtro (local, data ou distância) |
| **Base** | Usuários ativos (métrica 4) |
| **Janela** | Mensal |
| **Origem** | `Métricas de UX!13`. A planilha traz só "quantidade de pesquisas". ⚠️ **Proposta de operacionalização**: dividir pelo número de ativos, para comparar meses com bases de tamanhos diferentes |

#### 6. Frequência de uso da funcionalidade (acompanhamento do kit)
| | |
|---|---|
| **Cálculo** | `consultas ao acompanhamento do kit no período / corredores que consultaram o acompanhamento no período` |
| **Medição** | Consulta = abrir a linha do tempo do kit |
| **Base** | Corredores com kit em andamento |
| **Janela** | Mensal |
| **Origem** | `Métricas de Produto!52` |

### Adoption, Adoção

#### 7. Taxa de ativação
| | |
|---|---|
| **Cálculo** | `(corredores que fizeram a primeira inscrição paga em até 30 dias após o cadastro / corredores cadastrados no período) × 100` |
| **Medição** | Evento de ativação = primeira inscrição paga |
| **Base** | Coorte de cadastros do mês |
| **Janela** | 30 dias após o cadastro |
| **Origem** | `Métricas de Produto!15` (também em `!74`). ⚠️ A planilha traz só uma definição ("% de usuários que experimentaram a proposta de valor"). **Proposta a validar** |

#### 8. Taxa de conversão por etapa do funil
| | |
|---|---|
| **Cálculo** | `(corredores que chegaram à etapa seguinte / corredores elegíveis na etapa anterior) × 100`, para cada passagem: busca → detalhes da prova → início da inscrição → pagamento concluído |
| **Medição** | Corredores únicos por etapa |
| **Base** | Corredores que entraram na etapa anterior |
| **Janela** | Mensal |
| **Origem** | `Métricas de Produto!9`. ⚠️ A planilha divide a etapa 1 pela etapa 2, o que inverte a conversão. **Correção proposta**, não é a fórmula literal do Excel |

#### 9. % Adoção de funcionalidade (entrega do kit)
| | |
|---|---|
| **Cálculo** | `(corredores que escolheram "Receber em casa" ou "Ponto parceiro" / corredores que concluíram inscrição) × 100` |
| **Medição** | Base em corredores, não em inscrições: quem fez várias inscrições conta uma vez se usou a entrega em pelo menos uma |
| **Base** | Corredores com inscrição concluída no período |
| **Janela** | Mensal |
| **Origem** | `Métricas de Produto!56` |

### Retention, Retenção

#### 10. Taxa de retenção
| | |
|---|---|
| **Cálculo** | `(corredores da coorte que fizeram uma nova inscrição em até 12 meses após a primeira / corredores da coorte) × 100` |
| **Medição** | Coorte = corredores com a primeira inscrição paga no mesmo mês. Retorno = segunda inscrição paga |
| **Base** | Coorte mensal de primeiras inscrições |
| **Janela** | 12 meses. É a métrica da meta de 50% |
| **Origem** | `Métricas de Produto!20`. ⚠️ A planilha calcula retenção de clientes num período, sem coorte. **Redefinição proposta**, para medir recorrência por comportamento |

#### 11. Taxa de churn
| | |
|---|---|
| **Cálculo** | `(corredores ativos no início do período que ficaram 6 meses sem nova inscrição / corredores ativos no início do período) × 100` |
| **Medição** | Como não há assinatura, "cancelar" é definido como inatividade. Corredor ativo = pelo menos 1 inscrição nos 12 meses anteriores |
| **Base** | Corredores ativos no início do período |
| **Janela** | Semestral |
| **Origem** | `Métricas de Produto!30`. ⚠️ A planilha usa "clientes que cancelaram o serviço". **Proposta a validar**. Não é o inverso automático da retenção: base e janela são diferentes |

### Task Success, Sucesso em tarefas

#### 12. Taxa de sucesso na tarefa (inscrição)
| | |
|---|---|
| **Cálculo** | `(inscrições concluídas / inscrições iniciadas) × 100` |
| **Medição** | Tentativa = clique em "Inscrever-se". Sucesso = pagamento confirmado. Várias tentativas do mesmo corredor na mesma prova no mesmo dia contam como 1. Separar corredores com perfil PCD ativo para acompanhar a meta de acessibilidade |
| **Base** | Inscrições iniciadas |
| **Janela** | Mensal |
| **Origem** | `Métricas de UX!3` (também em `Métricas de Produto!31`) |

#### 13. Taxa de abandono (checkout)
| | |
|---|---|
| **Cálculo** | `(corredores que chegaram ao passo de pagamento e não concluíram / corredores que chegaram ao passo de pagamento) × 100` |
| **Medição** | Abandono = 30 minutos sem concluir |
| **Base** | Corredores que chegaram ao passo de pagamento |
| **Janela** | Mensal |
| **Origem** | `Métricas de Marketing!13`. A planilha descreve abandono de carrinho em e-commerce, adaptado aqui ao passo de pagamento |

#### 14. % de kits entregues no prazo *(métrica derivada do contexto)*
| | |
|---|---|
| **Cálculo** | `(kits entregues ou disponíveis para retirada até 2 dias antes da prova / kits com entrega ou ponto parceiro com prova no período) × 100` |
| **Medição** | Base em kits, não em corredores. Prazo = 2 dias antes da prova, como no protótipo |
| **Base** | Kits com entrega em casa ou ponto parceiro |
| **Janela** | Mensal |
| **Origem** | Não consta no catálogo. **Métrica proposta** a partir do diferencial do CorreAki, ligada à NSM sugerida |

---

## Resumo das métricas

| # | Frente | Métrica | Origem | Status |
|:---:|---|---|---|---|
| 1 | Happiness | CSAT do kit | Produto!33 | Catálogo |
| 2 | Happiness | NPS | Produto!34 | Catálogo |
| 3 | Happiness | CES da inscrição | UX!25 | Catálogo |
| 4 | Engagement | Usuários ativos | Produto!18 | ⚠️ Operacionalização |
| 5 | Engagement | Uso de busca interna | UX!13 | ⚠️ Operacionalização |
| 6 | Engagement | Frequência de uso (acompanhamento do kit) | Produto!52 | Catálogo |
| 7 | Adoption | Taxa de ativação | Produto!15 | ⚠️ Proposta a validar |
| 8 | Adoption | Taxa de conversão por etapa do funil | Produto!9 | ⚠️ Correção proposta |
| 9 | Adoption | % Adoção da entrega do kit | Produto!56 | Catálogo |
| 10 | Retention | Taxa de retenção | Produto!20 | ⚠️ Redefinição proposta |
| 11 | Retention | Taxa de churn | Produto!30 | ⚠️ Proposta a validar |
| 12 | Task Success | Taxa de sucesso na tarefa | UX!3 | Catálogo |
| 13 | Task Success | Taxa de abandono (checkout) | Marketing!13 | Adaptada |
| 14 | Task Success | % de kits entregues no prazo | - | Derivada do contexto |
