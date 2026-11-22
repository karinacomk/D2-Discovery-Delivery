# ✅ DoR e DoD — CorreAki

> **Origem**: [ondas.md](ondas.md), [roadmap.md](roadmap.md), [metricas-heart-correaki.md](metricas-heart-correaki.md) e [validacao.md](validacao.md)
> **Status**: proposta para o grupo validar com o Líder Técnico.

- **DoR (Definition of Ready)**: o que um cartão precisa ter para **entrar** em uma onda.
- **DoD (Definition of Done)**: o que um cartão precisa cumprir para ser considerado **pronto**.

---

## 🟢 Definition of Ready (DoR)

Um cartão só entra na onda quando cumpre **todos** os itens abaixo.

### História
- [ ] Escrita no formato **Como [persona], quero [ação], para [benefício]**, citando a persona ([Bianca](persona-bianca.md) ou [Valdir](persona-valdir.md)).
- [ ] O problema ou a dor que resolve está ligado a uma evidência: entrevista, jornada ou achado da [validação](validacao.md).
- [ ] Respeita o quadro [É / Não é · Faz / Não faz](e-nao-e-faz-nao-faz.md).

### Critérios de aceite
- [ ] Critérios escritos em **BDD** (Dado / Quando / Então), incluindo o caminho feliz e os principais erros.
- [ ] Casos de borda listados. Ex.: prova sem entrega disponível, CEP fora da área, inscrição duplicada na mesma prova.
- [ ] Critério de **acessibilidade** definido para telas da jornada de inscrição (meta de 20% de participação PCD).

### Design e regras
- [ ] Protótipo ou wireframe aprovado (pode partir do [protótipo no Lovable](https://corre-aki.lovable.app/)).
- [ ] Regras de negócio explícitas: preços, frete, prazos, cancelamento e reembolso, quando se aplicarem.
- [ ] Textos e mensagens de erro definidos.

### Viabilidade
- [ ] **Dependências** do cartão já entregues em ondas anteriores (regra 6 das [ondas](ondas.md)).
- [ ] Esforço (E) estimado pelo time e validado pelo Líder Técnico.
- [ ] Cartões de **confiança baixa** 🟥 passaram por um spike ou têm as dúvidas registradas e um dono para cada uma.
- [ ] Integrações externas (pagamento, logística, organizadores) com contato, documentação e ambiente de teste disponíveis.

### Dados e LGPD
- [ ] Dados pessoais coletados listados, com finalidade e base legal.
- [ ] Evento de métrica HEART que o cartão alimenta definido (ex.: conversão por etapa do funil, adoção da entrega do kit).

---

## 🏁 Definition of Done (DoD)

### Por cartão
- [ ] Todos os critérios de aceite atendidos e demonstrados ao PO.
- [ ] Código revisado por pelo menos 1 dev (pull request aprovado).
- [ ] Testes automatizados para as regras de negócio, com a pipeline verde.
- [ ] Testado em **web e mobile** (navegadores e tamanhos de tela combinados pelo time).
- [ ] **Acessibilidade**: navegação por teclado, leitor de tela e contraste conforme WCAG 2.1 nível AA.
- [ ] **LGPD**: dados sensíveis protegidos, consentimento registrado quando necessário e nenhum dado pessoal em logs.
- [ ] Eventos de métrica disparando e conferidos no ambiente de homologação.
- [ ] Mensagens de erro e estados vazios implementados (sem botão que parece clicável e não faz nada, achado da validação).
- [ ] Sem bugs críticos ou altos abertos.
- [ ] Documentação atualizada: regras de negócio, contratos de API e notas de versão.

### Por onda
- [ ] Todos os cartões da onda cumprem o DoD por cartão.
- [ ] **Semana de testes e homologação** concluída (prevista no [roadmap](roadmap.md)).
- [ ] Teste de regressão das ondas anteriores executado.
- [ ] Homologado pelo PO e publicado em produção.
- [ ] Ondas que mexem na inscrição ou no kit: teste de usabilidade com corredores reais, **incluindo corredores PCD**.
- [ ] Indicadores HEART da onda acompanhados no dashboard e comparados com a linha de base.

---

## Pontos para o grupo revisar

1. **Nível de acessibilidade**: WCAG 2.1 AA é a sugestão. O grupo pode decidir exigir isso só nas telas da inscrição ou em todo o produto.
2. **Spike para cartões 🟥**: o roadmap já soma +1 semana para confiança baixa. Vale decidir se essa semana é o spike ou se o spike acontece antes da onda.
3. **Teste com usuários reais por onda**: pode pesar no prazo de 3 semanas. Uma alternativa é fazer o teste a cada 2 ou 3 ondas.
