# Site Jogos 2026 — como publicar e atualizar

O site lê a planilha **Jogos_2026.xlsx** diretamente. Não existe banco de dados nem programa para rodar:
**para atualizar, basta substituir a planilha no GitHub.**

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | O site (não precisa mexer) |
| `Jogos_2026.xlsx` | A planilha de sempre — é dela que saem todos os números |
| `escudo.png` | *(opcional)* Escudo do time. Se enviar uma imagem com esse nome, ela aparece no topo |

## 1. Publicar pela primeira vez (uma vez só, ~10 minutos)

1. Crie uma conta grátis em **github.com** (se ainda não tiver).
2. Clique em **+ → New repository**.
   - *Repository name*: `jogos2026` (ou outro nome sem espaços)
   - Marque **Public** (o GitHub Pages gratuito exige repositório público)
   - Clique em **Create repository**.
3. Na página do repositório, clique em **uploading an existing file** (ou **Add file → Upload files**).
   Arraste `index.html` e `Jogos_2026.xlsx` (e `escudo.png`, se tiver) e clique em **Commit changes**.
4. Vá em **Settings → Pages**.
   Em *Build and deployment* → *Source*: **Deploy from a branch**; *Branch*: **main** e pasta **/ (root)** → **Save**.
5. Aguarde 1–2 minutos. O endereço aparece no topo da mesma página, no formato:
   `https://SEU-USUARIO.github.io/jogos2026/`

Esse é o link para mandar no grupo.

## 2. Atualizar toda semana (~1 minuto)

1. Lance o jogo na planilha como de costume (aba **Lançamentos**) e salve.
2. Abra o repositório no GitHub → **Add file → Upload files**.
3. Arraste o **Jogos_2026.xlsx** atualizado (**mesmo nome**) → **Commit changes**.
4. Em 1–2 minutos o site já mostra os novos números (se não aparecer, atualize a página).

Funciona pelo celular também (site do GitHub no navegador → mesmo caminho).

## Regras que o site segue (as mesmas da planilha)

- Placar = gols dos jogadores + gols contra do adversário.
- Rankings de jogadores contam **só jogos na linha**; rankings de goleiros, **só jogos no gol** (coluna **Goleiro = Sim**).
- Mínimo de presença: lido da célula amarela da aba **Classificação** (T3). Quem não atinge vai para o fim, em cinza.
- Convidados (Tipo = Convidado na aba **Jogadores**) aparecem em laranja.
- Desempates iguais aos da planilha.

## Avisos automáticos

Se faltar marcar o goleiro de um time, um jogador não estiver cadastrado ou houver gol sem nome, o site mostra
uma caixa amarela **"Conferir na planilha"** no topo. Corrija na planilha e envie de novo.

## Observações

- Não renomeie as abas **Lançamentos**, **Jogadores** e **Classificação** nem os títulos das colunas da aba Lançamentos.
- Se quiser trocar o nome da planilha ou o título do site, edite o bloco `CONFIG` no início do `<script>` do `index.html`.
- Como o repositório é público, qualquer pessoa com o link pode baixar a planilha.
- Abrir o `index.html` direto do computador (duplo clique) não funciona: o navegador bloqueia a leitura da planilha. Use o link do GitHub Pages.
