# 💬 FinChat — Controle suas finanças na conversa

> Um aplicativo de finanças pessoais criado para quem quer organizar o dinheiro sem o estresse de preencher planilhas ou formulários chatos.

---

## 💡 Sobre o Projeto

A maioria das pessoas desiste de anotar os próprios gastos pelo mesmo motivo: dá trabalho demais. Ter que abrir um app, escolher categoria, digitar data, valor e forma de pagamento a cada cafezinho comprado faz qualquer um perder a paciência.

O **FinChat** nasceu para mudar essa dinâmica. A proposta é simples: você registra tudo como se estivesse conversando com um amigo no WhatsApp. 

Você só manda mensagens como *"Almoço por R$ 38 no débito"* ou *"Recebi R$ 3.000 de salário"*, e o app entende sozinho o que aconteceu, organiza o gasto e atualiza seu saldo no mesmo instante.

### ✨ O que dá para fazer no app:
- **Conversar para registrar:** Basta digitar o que comprou ou recebeu do seu jeito.
- **Painel simples e direto:** Mostra o que entrou, o que saiu e quanto você ainda tem de forma limpa, sem termos complicados.
- **Metas visuais:** Barras de progresso para acompanhar a sua reserva de emergência ou aquela viagem dos sonhos.
- **Visual leve e limpo:** Feito para usar no celular, sem poluição visual ou menus escondidos.

---

## 🧠 O que aprendi construindo esse projeto

Criar esse aplicativo do zero usando ferramentas modernas de criação guiada por inteligência artificial me ensinou lições valiosas sobre como tirar ideias do papel hoje:

### 1. Saber o que quer vale mais do que apenas escrever código
A inteligência artificial ajuda muito na velocidade, mas ela só entrega algo bom se a pessoa souber exatamente o problema que quer resolver. Pensar na rotina de quem vai usar, nos exemplos reais do dia a dia e nas regras de cada tela foi o que fez o projeto realmente funcionar.

### 2. O olhar humano faz toda a diferença
Usar essas novas ferramentas não significa "deixar a máquina fazer tudo". O meu papel foi pensar como arquiteto do projeto: definir o design, testar a usabilidade, garantir que o visual ficasse agradável e decidir o que fazia ou não sentido para quem está usando.

### 3. Bom design é tirar obstáculos, não enfeitar a tela
A maior lição desse processo foi perceber que um bom produto é aquele que facilita a vida das pessoas. Trocar formulários complexos por uma conversa simples e usar palavras que todo mundo entende no lugar de jargões financeiros transformou uma tarefa chata em algo natural.

Prompt utilizado para a criação:

Crie uma aplicação web completa, moderna, responsiva (mobile-first) de Gestão de Finanças Pessoais chamada "FinChat", com prioridade absoluta em facilidade de uso, simplicidade extrema e uma estética minimalista/clean.

### 1. Diretrizes de Design Clean & Minimalista
- **Estética & Visual:**
  * Linhas limpas, cantos suavemente arredondados (rounded-xl) e bordas quase imperceptíveis (border-slate-100 / border-zinc-800).
  * Uso generoso de espaço em branco (respiro visual) para evitar qualquer sensação de tela poluída ou sobrecarregada.
  * Sombras sutis (soft shadows) apenas para dar leve profundidade aos cards interativos.
- **Paleta de Cores Serena:**
  * Fundo neutro limpo (branco off-white ou slate ultra-claro no modo claro; slate-900 fosco no dark mode).
  * Cores funcionais e suaves (não berrantes): verde esmeralda suave para entradas e progresso de metas; vermelho/coral delicado para despesas; azul/índigo acinzentado para destaques e botões de ação primária.
- **Tipografia e Hierarquia:**
  * Fonte sans-serif limpa e moderna (ex: Inter ou Geist), com pesos bem definidos (valores monetários em semibold grande para leitura imediata, descrições secundárias em tom muted/cinza).

### 2. Princípios de Usabilidade e Redução de Atrito (Prioridade Máxima)
- **Zero Complicação:** Nenhuma tela deve exigir mais do que 1 ou 2 toques para realizar a ação principal.
- **Linguagem Natural Sem Jargões:** Substituir termos técnicos de finanças por termos cotidianos ("O que entrou", "O que saiu", "Guardado", "Meu Saldo").
- **Navegação Intuitiva:**
  * Mobile: barra inferior (bottom navigation) fixa e minimalista com apenas 3 ícones claros: "Assistente", "Resumo" e "Metas".
  * Desktop: sidebar recolhível limpa e discreta.
- **Feedback Imediato e Reversibilidade:**
  * Toda transação criada exibe toast sutil de sucesso e card no chat com botão de "Desfazer", garantindo que o usuário nunca tenha medo de errar ou digitar algo errado.

### 3. Racional da Estrutura e Rotina do Usuário
- **Por que o Chat é o ponto de entrada primário:** O maior motivo de abandono de apps de finanças é a preguiça de preencher formulários com data, categoria e valor. O chat elimina formulários manuais: o usuário digita como se estivesse conversando no WhatsApp e a IA cuida da estruturação.
- **Por que sincronização em tempo real:** Ao confirmar uma mensagem, o saldo geral e o extrato são atualizados no mesmo instante, dando sensação imediata de controle.

### 4. Seção 1: Assistente Financeiro (Chat com Parsing Inteligente)
- Interface de chat limpa e arejada, sem elementos visuais concorrendo com as mensagens.
- Chips de atalho rápido acima do campo de texto (ex: "Gastei R$ 45 no almoço", "Salário R$ 3.000", "Guardar R$ 150 na Reserva").
- Exemplos de processamento e comportamento:
  * **Exemplo 1 (Despesa):**
    - Entrada: "Almoço por 38 reais no débito"
    - Processamento: Despesa | Alimentação | R$ 38,00 | Débito
    - Resposta: Card clean no chat: "Registrado com sucesso!" exibindo os dados organizados e opções de [Editar] e [Desfazer]. O saldo no dashboard é atualizado instantaneamente.
  * **Exemplo 2 (Receita):**
    - Entrada: "Recebi 3500 do meu salário"
    - Processamento: Receita | Salário | +R$ 3.500,00
    - Resposta: Card de confirmação com saldo atualizado em destaque.
  * **Exemplo 3 (Meta):**
    - Entrada: "Separei 200 reais pra viagem"
    - Processamento: Aporte na meta "Viagem" | R$ 200,00
    - Resposta: Confirmação com barra de progresso da meta avançando.
  * **Exemplo 4 (Dica prática):**
    - Entrada: "Como posso economizar este mês?"
    - Resposta: Sugestão amigável em tópicos curtos baseada no maior gasto mockado (ex: "Seus gastos com delivery estão em 35% do total. Pequenos ajustes nessa área podem liberar R$ 150 para sua Reserva").

### 5. Seção 2: Resumo Financeiro (Dashboard Clean)
- **Cards de Métricas:** Saldo Total destacado no topo em números grandes e legíveis, ladeado por pequenos indicadores discretos de Entradas e Saídas do mês.
- **Visualização Simples:**
  * Gráfico de rosca minimalista mostrando a divisão de gastos por categorias principais.
  * Mini gráfico de barras mostrando o ritmo de gastos dos últimos 7 dias.
- **Extrato Descomplicado:**
  * Lista de transações limpa: ícone discreto da categoria, nome simples, data relativa ("Hoje às 12:30", "Ontem") e valor em BRL.
  * Busca rápida no topo e filtro simples (Tudo, Entradas, Saídas).

### 6. Seção 3: Metas Simples
- Cards visuais objetivos com barra de progresso suave (ex: "Reserva de Emergência: R$ 6.000 / R$ 10.000 - 60%").
- Botão sutil "+ Nova Meta" que abre um modal minimalista de apenas 3 campos: Nome da Meta, Valor Desejado e Prazo.

### 7. Dados Mockados e Persistência
- Iniciar a aplicação pré-carregada com 6 transações realistas e 2 metas ativas.
- Salvar todos os novos registros em `localStorage` para não perder dados ao atualizar a página.
