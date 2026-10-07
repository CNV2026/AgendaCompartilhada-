# Agenda Compartilhada - Crédito Rural (GitHub Pages + Firebase)

Qualquer pessoa com o link abre, vê todos os agendamentos e agenda — sem login em conta nenhuma.

## 1. Criar o projeto Firebase (gratuito)
1. Acesse https://console.firebase.google.com → **Adicionar projeto** → nome: `agenda-credito-rural` (pode desligar o Google Analytics).

## 2. Ativar o banco de dados
1. Menu **Build → Firestore Database → Criar banco de dados**.
2. Local: `southamerica-east1 (São Paulo)`. Modo: **produção**.
3. Aba **Regras** → apague tudo, cole o conteúdo de `firestore.rules` → **Publicar**.

## 3. Ativar acesso anônimo (sem login para o usuário)
1. **Build → Authentication → Começar → Anônimo → Ativar → Salvar**.
   (O colaborador não vê nada disso: o navegador recebe um identificador invisível, que permite a cada pessoa excluir só o que ela mesma criou.)

## 4. Pegar a configuração
1. Engrenagem ⚙ → **Configurações do projeto** → role até **Seus aplicativos** → ícone **</>** (Web) → registre (nome livre; NÃO precisa de Hosting).
2. Copie os valores `apiKey`, `authDomain`, `projectId`, `appId` e cole em `firebase-config.js`.
   (Essa chave é pública por natureza; quem protege os dados são as regras do passo 2.)

## 5. Publicar no GitHub Pages
1. Crie um repositório no GitHub e envie `index.html` e `firebase-config.js`.
2. **Settings → Pages → Branch: main / (root) → Save**.
3. Em ~1 minuto o link `https://SEU-USUARIO.github.io/NOME-DO-REPO/` está no ar. É esse link que vai para os colegas.

## 6. Autorizar o domínio
Firebase → **Authentication → Configurações → Domínios autorizados → Adicionar** `SEU-USUARIO.github.io`.

## Limites do plano gratuito
50 mil leituras/dia e 20 mil gravações/dia: sobra para centenas de colaboradores.
