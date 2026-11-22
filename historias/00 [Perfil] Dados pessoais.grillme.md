# 🔥 Grill-me · [Perfil] Dados pessoais

> **História**: [00 [Perfil] Dados pessoais.md](00%20%5BPerfil%5D%20Dados%20pessoais.md) · **Testes**: [00 [Perfil] Dados pessoais.teste.md](00%20%5BPerfil%5D%20Dados%20pessoais.teste.md)
> **Data**: 22/11/2026

## Contexto e base
- Print da seção "Dados pessoais" do protótipo no Lovable, enviado pela PM.
- [prompt-lovable-correaki.md](../prompt-lovable-correaki.md): campos do cadastro e do passo 2 da inscrição; perfil com seções editáveis.
- [ondas.md](../ondas.md): cartão "Dados pessoais", Onda 7, confiança alta. O cartão "Alertas de alteração de cadastro" (Onda 10) depende dele.
- [dor-dod.md](../dor-dod.md): exigências de LGPD e acessibilidade.
- Sem Figma. O produto tem um único perfil de usuário: o corredor.

## Decisões antes do grill
| Pergunta | Resposta | Vira |
|---|---|---|
| CPF e e-mail podem ser editados? | CPF bloqueado; e-mail só com confirmação | RN02, RN03, RN04 |
| Opções de Sexo | Feminino, Masculino, Prefiro não informar | Campos |
| Data de nascimento, sexo e camiseta são obrigatórios? | Opcionais no perfil, exigidos na inscrição | RN08 |
| Alteração afeta inscrições já feitas? | Só vale para novas inscrições | RN09 |

## Rodada grill-me
| # | Pergunta | Resposta | Vira |
|---|---|---|---|
| 1 | Como salvar e o que acontece ao sair sem salvar? | Botão "Salvar alterações" ativo só com mudança; aviso ao sair | RN10 |
| 2 | Idade mínima | 18 anos para ter conta; rejeita data futura ou acima de 100 anos | RN07 |
| 3 | Tamanhos de camiseta | PP, P, M, G, GG, XGG | Campos |
| 4 | Gera notificação ao alterar dados? | Não nesta história (cartão da Onda 10) | RN12 |
| 5 | Salvamento parcial se um campo for inválido? | Tudo ou nada *(proposta pelo agente)* | RN11 |
| 6 | Quem pode ver e alterar? | Só o próprio corredor, validado também no servidor *(proposta pelo agente)* | RN01 |

## Pendências
1. **Textos propostos pelo agente, precisam de validação**: todas as mensagens da seção 5 e as mensagens de sucesso e de troca de e-mail.
2. **Validade do link de troca de e-mail (24 h)** e aviso ao e-mail antigo: proposta pelo agente, precisa de validação.
3. **Regras de nome e celular** (nome e sobrenome, até 100 caracteres; celular com 11 dígitos começando com 9): proposta pelo agente.
4. **Divergências do protótipo**: o Lovable mostra o CPF editável, não tem botão de salvar visível, não tem "Prefiro não informar" em Sexo e não tem XGG na camiseta. O protótipo precisa ser ajustado.
5. **"Prefiro não informar" × categorias por sexo**: se a prova premia por categoria de sexo, o que a inscrição pede? Precisa de decisão de produto (impacta o passo 2 da inscrição).
6. **Menores de 18 anos**: ficam fora do produto. Validar com o grupo se há provas infantis ou juvenis no escopo.
7. **Dúvida técnica**: como o servidor guarda o e-mail pendente de confirmação e o que acontece se o corredor pedir a troca duas vezes (sugestão: vale o último pedido).
