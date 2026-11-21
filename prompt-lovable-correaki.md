# Prompt para o Lovable — CorreAki

> **Base**: [correaki-one-pager.md](correaki-one-pager.md)
> **Como usar**: copie tudo o que está dentro do bloco abaixo e cole no Lovable.

```
Crie agora o app completo descrito abaixo. Não faça perguntas e não peça confirmação: todas as decisões já estão definidas aqui. Se algo não estiver especificado, escolha a opção mais simples e siga em frente.

# CorreAki

App web responsivo, mobile-first, todo em português do Brasil, com moeda em reais (R$ 0,00) e datas no formato DD/MM/AAAA.

## Produto
O CorreAki é uma plataforma para corredores de rua encontrarem corridas de vários organizadores em um só lugar, se inscreverem e receberem o kit da prova em casa ou retirá-lo em um ponto parceiro, em vez de depender do local e da data definidos pelo organizador. Busca, inscrição e entrega do kit ficam em uma única jornada, com acompanhamento de cada etapa.
Slogan exibido no topo da tela inicial: "Encontre sua corrida. Receba seu kit."

## Público
- Bianca, 25 anos, corredora iniciante, mora em Mogi das Cruzes (SP). Quer fazer a primeira prova de 5 km e não sabe por onde começar.
- Valdir, 45 anos, corredor experiente, mora em São Paulo. Busca provas de 21 km e 42 km e não consegue retirar o kit nos locais e datas do organizador.

## Tecnologia
- React + TypeScript + Tailwind + shadcn/ui.
- Sem backend nesta versão: todos os dados ficam em arquivos de dados mockados no front e o estado (usuário logado, inscrições, notificações) é salvo no localStorage.
- Login simulado: qualquer e-mail válido e senha com 6 ou mais caracteres entram. Já deixe logado o usuário de exemplo "Bianca Souza" (bianca@exemplo.com / 123456).
- Pagamento simulado: ao confirmar, aguardar 1,5 segundo com indicador de carregamento e aprovar.

## Identidade visual
- Cor principal: #FF5A1F (laranja). Hover: #E04812.
- Cor de apoio: #1B1F3B (azul-marinho), usada no cabeçalho e nos títulos.
- Sucesso: #16A34A. Alerta: #F59E0B. Erro: #DC2626.
- Fundo: #F7F7F8. Cards: #FFFFFF com borda #E5E7EB, cantos arredondados de 12px e sombra leve.
- Fontes: "Montserrat" (700 e 800) para títulos e "Inter" (400, 500 e 600) para textos, via Google Fonts.
- Ícones: lucide-react.
- Imagens das corridas: fotos de corrida de rua do Unsplash.
- Logo: texto "CorreAki" em Montserrat 800, com "Aki" na cor principal, ao lado de um ícone de tênis de corrida.

## Navegação
- Celular: barra inferior fixa com 4 abas: Início (ícone casa), Inscrições (ícone ticket), Notificações (ícone sino, com contador de não lidas) e Perfil (ícone usuário).
- Desktop (a partir de 768px): cabeçalho fixo azul-marinho com logo à esquerda e as mesmas 4 opções à direita.
- Rodapé em todas as páginas com links "Termos de uso" e "Política de privacidade".

## Rotas
/login, /cadastro, /recuperar-senha, / (início), /corrida/:id, /inscricao/:id, /inscricao/:id/confirmacao, /inscricoes, /inscricoes/:id, /notificacoes, /notificacoes/configuracoes, /perfil, /termos, /privacidade

## Telas

### 1. Login, cadastro e recuperação de senha
- Login: e-mail, senha, botão "Entrar", links "Esqueci minha senha" e "Criar conta".
- Cadastro: nome completo, e-mail, CPF (com máscara), celular (com máscara), senha, confirmar senha e caixa obrigatória "Li e aceito os Termos de uso e a Política de privacidade" (com links).
- Recuperar senha: campo de e-mail e botão "Enviar link". Depois exibir "Enviamos um link para o seu e-mail."
- Botão "Sair" no Perfil volta para /login.

### 2. Início (calendário de corridas)
- Saudação "Olá, Bianca!" e slogan.
- Barra de busca por texto (nome da corrida, cidade ou organizador).
- Filtros em chips: Estado (Todos, SP, RJ, MG), Distância (5 km, 10 km, 21 km, 42 km, seleção múltipla), Período (Este mês, Próximos 3 meses, Próximos 6 meses) e o chip "Minha primeira corrida" (mostra só provas com selo de iniciante).
- Botão "Limpar filtros" e contador "X corridas encontradas".
- Lista de cards em grade (1 coluna no celular, 2 no tablet, 3 no desktop), ordenada pela data mais próxima. Cada card: foto, nome, data, cidade/UF, chips de distâncias, "a partir de R$ X", nome do organizador e selos "Entrega do kit" (verde) e "Boa para iniciantes" (laranja, quando aplicável).
- Estado vazio: "Nenhuma corrida encontrada com esses filtros." com botão "Limpar filtros".

### 3. Detalhes da corrida
- Foto grande, nome, data, horário da largada, local da largada, cidade/UF e organizador.
- Tabela de distâncias com preço e vagas restantes; distância esgotada aparece desabilitada com o texto "Esgotado".
- Seções: "Sobre a prova", "Percurso", "O que vem no kit", "Retirada no organizador" (local, datas e horários), "Acessibilidade" (recursos da prova) e "Como funciona" (3 passos: 1. Escolha a distância e se inscreva; 2. Receba o kit em casa ou retire num ponto parceiro; 3. Corra e acompanhe tudo pelo app).
- Botão fixo no rodapé da tela: "Inscrever-se".

### 4. Inscrição (4 passos com barra de progresso)
- Passo 1, Distância: cards selecionáveis com distância e preço.
- Passo 2, Dados do corredor: nome, CPF, data de nascimento, sexo, tamanho da camiseta (PP, P, M, G, GG), contato de emergência (nome e telefone). Pré-preencher com os dados do perfil.
- Passo 3, Kit: três opções em cards:
  a) "Receber em casa": campos de CEP, rua, número, complemento, bairro, cidade, UF. Frete: R$ 14,90 para a mesma cidade da prova, R$ 24,90 para outra cidade do mesmo estado e R$ 34,90 para outro estado. Prazo: entrega até 2 dias antes da prova.
  b) "Retirar em ponto parceiro": lista de pontos parceiros da cidade da prova (nome, endereço, horário). Taxa: R$ 7,90.
  c) "Retirar no organizador": mostra local e datas do organizador. Sem custo.
- Passo 4, Pagamento: resumo (corrida, distância, valor da inscrição, valor do kit, desconto, total), campo de cupom e escolha entre "Cartão de crédito" (número, nome, validade, CVV, parcelas de 1x a 3x sem juros) e "Pix" (exibir QR Code fictício e botão "Copiar código").
  Cupons válidos: PRIMEIRACORRIDA (15% de desconto na inscrição) e CORREAKI10 (R$ 10,00 de desconto). Cupom inválido mostra "Cupom inválido ou expirado".
- Validar cada passo antes de avançar, com mensagens de erro abaixo de cada campo. Botões "Voltar" e "Continuar"; no último passo, "Pagar R$ X".
- Confirmação: ícone de sucesso, "Inscrição confirmada!", número do pedido (CA-000123), resumo e botões "Acompanhar meu kit" e "Voltar ao início". Criar uma notificação de compra confirmada.

### 5. Minhas inscrições
- Abas "Próximas" e "Passadas".
- Cards com foto, nome da corrida, data, distância e status do kit em um selo colorido.
- Detalhe da inscrição:
  - Dados da inscrição e número do pedido.
  - Linha do tempo vertical do kit, com data e hora de cada etapa concluída:
    Entrega em casa: Inscrição confirmada → Kit separado → Kit a caminho → Kit entregue.
    Ponto parceiro ou organizador: Inscrição confirmada → Kit separado → Pronto para retirada → Kit retirado.
  - Previsão de entrega ou endereço do ponto de retirada.
  - Botões: "Alterar endereço de entrega" (só enquanto o status for "Inscrição confirmada" ou "Kit separado"), "Transferir inscrição" (modal com nome, CPF e e-mail do novo titular) e "Cancelar inscrição" (modal de confirmação dentro da página informando reembolso de 100% até 7 dias antes da prova e 50% depois disso).
  - Cada ação gera uma notificação e mostra um toast de sucesso.

### 6. Perfil do corredor
- Foto (avatar com iniciais), nome, cidade e "Corredor desde 2026".
- Pontuação e ranking: "1.250 pontos · 87º no ranking de SP", com regra exibida: 100 pontos por inscrição e 50 por prova concluída. Lista com o top 5 do ranking.
- Seções editáveis: Dados pessoais, Endereço, Objetivos (opções: "Completar minha primeira prova de 5 km", "Correr 10 km", "Fazer uma meia maratona", "Fazer uma maratona", "Melhorar meu tempo") e Histórico de corridas (nome, data, distância e tempo).
- Seção "Acessibilidade": pergunta "Você é uma pessoa com deficiência?" (Sim/Não). Se Sim, caixas: deficiência física, visual, auditiva, intelectual, outra; e caixas de necessidade: guia de corrida, cadeira de rodas, intérprete de Libras, área reservada na largada. Quando preenchida, o detalhe da corrida destaca os recursos de acessibilidade compatíveis.
- Links "Configurar notificações", "Termos de uso", "Política de privacidade", botão "Sair" e botão "Excluir conta" (modal de confirmação dentro da página).

### 7. Notificações
- Lista com ícone por tipo, título, texto, data relativa ("há 2 horas") e destaque para não lidas. Botão "Marcar todas como lidas".
- Tipos: Compra, Entrega do kit, Cadastro, Cancelamento e Avisos da prova.
- Configurações: um interruptor para cada tipo, todos ligados por padrão.

### 8. Termos de uso e Política de privacidade
- Duas páginas de texto com títulos e seções: coleta de dados, uso dos dados, compartilhamento com organizadores e parceiros de entrega, direitos do titular (LGPD), contato do encarregado (dpo@correaki.com.br).

## Dados mockados
Corridas (12), todas com foto, descrição, percurso, itens do kit (camiseta, número de peito, chip, medalha de participação e sacochila), local de retirada no organizador e recursos de acessibilidade:
1. Corrida das Flores — Mogi das Cruzes/SP — 5 km e 10 km — R$ 89,00 — Mogi Run Eventos — iniciante
2. Night Run Paulista — São Paulo/SP — 5 km e 10 km — R$ 129,00 — Paulista Sports — iniciante
3. Meia Maratona de São Paulo — São Paulo/SP — 21 km — R$ 189,00 — SP Corre
4. Maratona de São Paulo — São Paulo/SP — 42 km — R$ 259,00 — SP Corre
5. Circuito das Estações: Verão — São Paulo/SP — 5 km e 10 km — R$ 119,00 — Estações Run — iniciante
6. Corrida do Parque Vicentina Aranha — São José dos Campos/SP — 5 km e 10 km — R$ 95,00 — Vale Corre — iniciante
7. Desafio da Serra — Campos do Jordão/SP — 10 km e 21 km — R$ 169,00 — Serra Eventos
8. Meia Maratona do Rio — Rio de Janeiro/RJ — 21 km — R$ 199,00 — Rio Run
9. Maratona do Rio — Rio de Janeiro/RJ — 42 km — R$ 279,00 — Rio Run
10. Corrida da Orla — Niterói/RJ — 5 km e 10 km — R$ 99,00 — Orla Eventos — iniciante
11. Volta da Pampulha — Belo Horizonte/MG — 10 km e 18 km — R$ 149,00 — BH Esportes
12. Corrida das Montanhas — Ouro Preto/MG — 10 km e 21 km — R$ 159,00 — Minas Trail
Distâncias maiores custam R$ 30,00 a mais que a menor. Datas distribuídas nos próximos 6 meses a partir de hoje. A Corrida das Flores tem a distância de 10 km esgotada.

Pontos parceiros: 2 por cidade das corridas, com nomes como "Loja Corre Mais" e "Academia Ritmo".

Usuária de exemplo: Bianca Souza, CPF 123.456.789-00, Mogi das Cruzes/SP, objetivo "Completar minha primeira prova de 5 km", 1.250 pontos, 87º no ranking de SP, com:
- Inscrição na Corrida das Flores (5 km), entrega em casa, status "Kit a caminho".
- Inscrição no Circuito das Estações (5 km), retirada em ponto parceiro, status "Inscrição confirmada".
- Histórico: 1 prova concluída, "Corrida de Natal Mogi, 5 km, 00:34:12".
- 5 notificações, 2 não lidas.

## Acessibilidade
Contraste WCAG AA, textos alternativos em todas as imagens, navegação completa por teclado, foco visível, área de toque mínima de 44px, rótulos em todos os campos de formulário, mensagens de erro associadas aos campos e respeito a prefers-reduced-motion.

## Fora do escopo
Não criar: organização de eventos, registro de treinos, suporte durante a prova, outros esportes, painel do organizador, integração real com pagamento ou entrega.
```
