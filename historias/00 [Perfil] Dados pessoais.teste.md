# 🧪 Testes · [Perfil] Dados pessoais

> **História**: [00 [Perfil] Dados pessoais.md](00%20%5BPerfil%5D%20Dados%20pessoais.md) · **Grill-me**: [00 [Perfil] Dados pessoais.grillme.md](00%20%5BPerfil%5D%20Dados%20pessoais.grillme.md)

## Seams (pontos de teste)
| Seam | O que testa |
|---|---|
| **VAL** | Validação dos campos (tela e servidor) |
| **SAV** | Salvar e descartar alterações |
| **EML** | Fluxo de troca de e-mail |
| **SEG** | Acesso e campos bloqueados no servidor |
| **INS** | Integração com o passo 2 da inscrição |
| **A11Y** | Acessibilidade e LGPD |

## Matriz de rastreabilidade
| Regra / Cenário | Casos |
|---|---|
| RN01 | SEG-01 |
| RN02 · Cenário 4 | SEG-02, SEG-03 |
| RN03 · Cenário 2 | EML-01, EML-02, EML-03 |
| RN04 | EML-04 |
| RN05 | VAL-01 |
| RN06 | VAL-02 |
| RN07 · Cenário 3 | VAL-03, VAL-04 |
| RN08 · Cenário 5 | INS-01, INS-02 |
| RN09 · Cenário 6 | INS-03 |
| RN10 · Cenário 7 | SAV-02, SAV-03 |
| RN11 | SAV-04 |
| RN12 | SAV-05 |
| RN13 | A11Y-01, A11Y-02 |
| RN14 · Cenário 8 | SAV-07 |
| RN15 | EML-05, EML-06 |
| Cenário 1 | SAV-01 |
| Falha de conexão | SAV-06 |

## Casos

### VAL · Validação
**VAL-01** 🔴 Nome completo
- **Dado** o campo Nome com "Bianca" · **Quando** salva · **Então** exibe *"Informe nome e sobrenome."* e não salva. Repetir com 101 caracteres e com vazio.
- Ref: RN05

**VAL-02** 🔴 Celular
- **Dado** o celular "(11) 8888-1234" ou "(00) 99999-1234" · **Quando** salva · **Então** exibe *"Informe um celular válido com DDD."*
- Ref: RN06

**VAL-03** 🔴 Idade mínima
- **Dado** uma data de nascimento de quem completa 18 anos amanhã · **Quando** salva · **Então** exibe *"É preciso ter 18 anos ou mais para usar o CorreAki."* Com 18 anos completos hoje, salva.
- Ref: RN07, Cenário 3

**VAL-04** 🟡 Datas inválidas
- **Dado** uma data futura ou de mais de 100 anos atrás · **Quando** salva · **Então** exibe *"Informe uma data de nascimento válida."*
- Ref: RN07

### SAV · Salvar e descartar
**SAV-01** 🔴 Salvar com sucesso
- **Dado** celular e camiseta alterados · **Quando** clica em "Salvar alterações" · **Então** salva, exibe *"Dados atualizados."* e o botão fica inativo.
- Ref: Cenário 1

**SAV-02** 🟡 Botão inativo sem mudanças
- **Dado** a tela recém-aberta, ou um campo alterado e depois devolvido ao valor original · **Então** "Salvar alterações" fica inativo.
- Ref: RN10

**SAV-03** 🟡 Aviso ao sair
- **Dado** um campo alterado sem salvar · **Quando** tenta sair · **Então** pergunta *"Descartar alterações?"*; "Continuar editando" mantém os dados, "Descartar" sai sem salvar.
- Ref: RN10, Cenário 7

**SAV-04** 🔴 Tudo ou nada
- **Dado** um celular válido e uma data de nascimento inválida · **Quando** salva · **Então** nenhum dos dois é salvo.
- Ref: RN11

**SAV-05** 🟢 Sem notificação
- **Dado** um salvamento com sucesso · **Então** nenhuma notificação é criada na central de notificações.
- Ref: RN12

**SAV-06** 🟡 Falha de conexão
- **Dado** que o servidor não responde · **Quando** salva · **Então** exibe *"Não foi possível salvar agora. Tente novamente."* e os dados digitados continuam na tela.
- Ref: Seção 5

**SAV-07** 🔴 Edição em dois aparelhos
- **Dado** a tela aberta no computador e uma alteração salva depois pelo celular · **Quando** salva pelo computador · **Então** exibe *"Seus dados foram alterados em outro acesso. Recarregue a página."* e mantém os dados do celular.
- Ref: RN14, Cenário 8

### EML · Troca de e-mail
**EML-01** 🔴 Pedido de troca
- **Dado** um e-mail novo e livre · **Quando** salva · **Então** envia o link ao novo e-mail, avisa o antigo, exibe a mensagem de confirmação, e o login continua no e-mail antigo.
- Ref: RN03, Cenário 2

**EML-02** 🔴 Confirmação
- **Dado** o link recebido · **Quando** clica dentro de 24 h · **Então** o e-mail da conta passa a ser o novo.
- Ref: RN03

**EML-03** 🟡 Link expirado
- **Dado** um link com mais de 24 h · **Quando** clica · **Então** exibe *"Este link expirou. Peça a troca de e-mail de novo no seu perfil."* e mantém o e-mail antigo.
- Ref: RN03

**EML-04** 🔴 E-mail em uso
- **Dado** um e-mail já usado por outra conta · **Quando** salva · **Então** exibe *"Este e-mail não pode ser usado. Tente outro."* sem revelar a outra conta.
- Ref: RN04

**EML-05** 🟡 Limite de pedidos
- **Dado** 5 pedidos de troca na última hora · **Quando** faz o 6º · **Então** exibe *"Você fez muitos pedidos de troca de e-mail. Tente de novo mais tarde."* e não envia link.
- Ref: RN15

**EML-06** 🟡 Link sem login e pedido substituído
- **Dado** o link aberto em outro aparelho, sem login · **Então** a troca é confirmada. **Dado** dois pedidos seguidos · **Quando** abre o link do primeiro · **Então** exibe *"Este link expirou..."*.
- Ref: RN15, RN03

### SEG · Acesso
**SEG-01** 🔴 Dados de outra conta
- **Dado** o corredor A logado · **Quando** pede ao servidor os dados ou a alteração da conta B · **Então** o pedido é recusado.
- Ref: RN01

**SEG-02** 🔴 CPF bloqueado na tela
- **Dado** a tela Dados pessoais · **Então** o CPF aparece com máscara e não pode ser editado.
- Ref: RN02, Cenário 4

**SEG-03** 🔴 CPF bloqueado no servidor
- **Dado** um pedido direto ao servidor com CPF diferente · **Então** o CPF não muda.
- Ref: RN02, Cenário 4

### INS · Inscrição
**INS-01** 🔴 Pré-preenchimento
- **Dado** um perfil completo · **Quando** chega ao passo 2 da inscrição · **Então** todos os campos vêm preenchidos com os dados do perfil.
- Ref: RN08, Cenário 5

**INS-02** 🔴 Perfil incompleto
- **Dado** um perfil sem data de nascimento · **Quando** chega ao passo 2 · **Então** o campo vem vazio e é obrigatório para continuar.
- Ref: RN08, Cenário 5

**INS-03** 🔴 Inscrição existente preservada
- **Dado** uma inscrição feita com camiseta "M" · **Quando** muda o perfil para "G" · **Então** a inscrição continua com "M".
- Ref: RN09, Cenário 6

### A11Y · Acessibilidade e LGPD
**A11Y-01** 🟡 Leitor de tela e teclado
- **Dado** a tela com leitor de tela · **Então** todo campo tem rótulo, os erros são anunciados e ligados ao campo, e a tela funciona só com teclado.
- Ref: RN13

**A11Y-02** 🟡 Dados fora dos logs
- **Dado** um salvamento · **Então** os logs não contêm nome, CPF, e-mail, celular nem data de nascimento.
- Ref: RN13
