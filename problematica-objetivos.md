# 🏃 Problemática — Busca de Corridas e Retirada de Kit

> **Origem**: dinâmica D² [do Discovery ao Delivery], quadro "Como podemos" + "Três objetivos para o negócio".
> **Estágio**: hipótese, baseada na experiência do time. Ainda não validada com corredores.
> **Data**: 20/11/2026

---

## 1. Declaração do problema (Como podemos)

| Verbo | O quê | Para quem |
|---|---|---|
| **Viabilizar** | a busca de corridas de rua e a retirada de kit | corredores de rua |

> **Como podemos viabilizar a busca de corridas de rua e a retirada de kit para corredores de rua?**

---

## 2. Contexto

A jornada do corredor de rua antes da prova tem dois momentos de atrito, que hoje não se conectam:

**Descobrir a corrida**
- As informações sobre provas (data, local, distância, preço, prazo de inscrição) estão espalhadas por sites de inscrição, Instagram, grupos de WhatsApp e assessorias.
- O corredor perde provas por não ficar sabendo a tempo, ou gasta tempo comparando fontes diferentes.

**Retirar o kit**
- A retirada costuma acontecer 1 ou 2 dias antes da prova, em local e horário fixos, quase sempre em horário comercial.
- Exige deslocamento, que pode ser grande para quem mora longe ou vem de outra cidade.
- Há filas, principalmente no último dia.
- Para outra pessoa retirar, é preciso autorização assinada e cópia de documento, com regras que mudam de evento para evento.

```
Descobrir a corrida → Inscrever-se → Retirar o kit → Correr
   ⚠️ informação            ⚠️ local/horário fixos,
      espalhada                fila, burocracia
```

---

## 3. Para quem

**Público principal**: corredores de rua que participam de provas ao longo do ano.

**Recorte prioritário** (objetivo 3): **corredores PCD** (pessoas com deficiência). Para eles, deslocamento, filas e locais pouco acessíveis pesam ainda mais, e a informação sobre acessibilidade da prova (categorias, guias, estrutura) costuma ser escassa.

---

## 4. Objetivos de negócio

Objetivos como foram escritos no quadro, com uma proposta de refinamento para torná-los mensuráveis.

| # | No quadro | Eixo | Proposta de refinamento |
|---|---|---|---|
| 1 | Garantir recorrência dos participantes em 50% por 12 meses | Retenção / churn | **50% dos corredores que se inscreverem em uma prova pela plataforma voltam a se inscrever em outra prova em até 12 meses.** |
| 2 | Fidelizar o usuário final para boa experiência do kit | Satisfação / fidelização | **Atingir NPS ≥ 50 (ou CSAT ≥ 4,5/5) na experiência de retirada do kit, medido após cada prova.** |
| 3 | Tornar a experiência acessível para o público PCD com 20% de participação | Inclusão / crescimento | **Fazer com que corredores PCD representem 20% de [base a definir] em até 12 meses**, com a jornada de busca e retirada acessível (WCAG AA no digital e opção de retirada acessível). |

### Observações sobre os objetivos

- **Objetivo 1**: está bem formulado (tem meta e prazo). Falta definir o que conta como "recorrência": nova inscrição, nova retirada de kit ou só voltar a buscar provas. A recomendação é contar **nova inscrição**, porque é o que gera receita.
- **Objetivo 2**: hoje está descrito como intenção, sem métrica. Precisa de um indicador (NPS, CSAT ou tempo médio de retirada) e de uma meta.
- **Objetivo 3**: o "20% de participação" precisa de uma base. 20% dos usuários da plataforma? Dos inscritos por prova? Para comparação, segundo o IBGE (PNAD 2022), cerca de 8,9% da população brasileira tem alguma deficiência. Uma meta de 20% é muito ambiciosa se a base for todos os usuários, e mais realista se for, por exemplo, "20% das provas listadas com categoria e estrutura PCD".
- **Equilíbrio**: os três objetivos cobrem retenção, experiência e inclusão. **Ainda não há um objetivo de receita/ROI** (por exemplo, receita por kit entregue ou LTV/CAC). Vale decidir se ele entra agora ou numa fase seguinte.

---

## 5. Hipóteses a validar

| # | Hipótese | Como validar |
|---|---|---|
| H1 | Corredores perdem provas ou gastam tempo demais por causa da informação espalhada. | Entrevistas com 5 a 8 corredores, perguntando sobre a última prova que perderam ou quase perderam. |
| H2 | A retirada presencial do kit é a etapa mais desgastante antes da prova. | Entrevistas e pesquisa rápida: tempo gasto, deslocamento, filas. |
| H3 | A burocracia da retirada por terceiros faz corredores desistirem ou se estressarem. | Entrevistas e análise das regras de 5 a 10 eventos. |
| H4 | Corredores PCD enfrentam barreiras específicas na busca e na retirada. | Entrevistas com corredores PCD e assessorias especializadas. |
| H5 | Uma boa experiência na retirada do kit aumenta a chance de o corredor voltar (liga o objetivo 2 ao objetivo 1). | Comparar a recorrência de quem avaliou bem a retirada com a de quem avaliou mal, após o MVP. |

---

## 6. Premissas e riscos

- **Dependência do organizador**: o formato da retirada do kit é decidido pelo organizador da prova. Mesmo com foco no corredor, qualquer mudança na retirada exige a adesão dele.
- **Concorrência**: já existem plataformas de inscrição e calendários de corrida (por exemplo, Ticket Sports e Minhas Inscrições). É preciso entender **por que elas não resolvem** a busca: listas incompletas, cada site mostra só as próprias provas, ou busca ruim.
- **Interesse do organizador na retirada presencial**: a expo de retirada gera visibilidade para patrocinadores. Esse ganho pode criar resistência a alternativas.

---

## 7. Fora do escopo (por enquanto)

- Inscrição e pagamento da prova dentro da plataforma.
- Ferramentas de gestão para organizadores.
- Acompanhamento de treinos e resultados.

---

## 8. Próximos passos

1. Fechar as definições pendentes dos objetivos 1, 2 e 3 (ver seção 4).
2. Rodar entrevistas para validar as hipóteses H1 a H4.
3. Mapear os concorrentes e por que não resolvem a busca.
4. Com as hipóteses validadas, seguir para o PRD (`/prd-ux`) ou para o One-Pager (`/one-pager-produto`).
