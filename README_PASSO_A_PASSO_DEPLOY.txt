CO-SAFE AI (HFACS-MAP) – PASSO A PASSO COMPLETO PARA PUBLICAR NA INTERNET

Este pacote foi preparado para o caminho mais fácil:
PUBLICAR NO STREAMLIT COMMUNITY CLOUD.

Assim, seu app poderá ser acessado de qualquer computador pelo navegador, sem precisar deixar o seu PC ligado.

============================================================
1. O QUE JÁ FOI FEITO NESTE PACOTE
============================================================

Este pacote já foi ajustado para deploy com:

1) requirements.txt
2) runtime.txt
3) .streamlit/config.toml
4) .gitignore
5) exemplo de secrets em .streamlit/secrets.toml.exemplo
6) app.py ajustado para:
   - aceitar OPENAI_API_KEY via Streamlit Secrets
   - ler PDF enviado pelo usuário
   - ler DOCX enviado pelo usuário
   - ler XLSX enviado pelo usuário
   - tentar ler XLS enviado pelo usuário
   - localizar melhor a logo da UFRJ

============================================================
2. ESTRUTURA DO PROJETO
============================================================

Mantenha exatamente esta estrutura:

00. APP HFACS-ACCIMAPS/
  00. Suporte ao APP/
  01. APP/
    app.py
  02. Figuras e Layout/
  03. Teste/
  .streamlit/
    config.toml
    secrets.toml.exemplo
  requirements.txt
  runtime.txt
  .gitignore
  README_PASSO_A_PASSO_DEPLOY.txt

IMPORTANTE:
Não mude o nome das pastas internas por enquanto.
Seu código depende dessa organização.

============================================================
3. O QUE VOCÊ VAI PRECISAR
============================================================

Você vai precisar de 3 coisas:

1) Uma conta no GitHub
2) Uma conta no Streamlit Community Cloud
3) Sua chave da OpenAI

Se ainda não tiver:
- GitHub: crie sua conta
- Streamlit Cloud: entre usando sua conta GitHub
- OpenAI API Key: copie sua chave e guarde

============================================================
4. PASSO A PASSO MAIS FÁCIL DE TODOS
============================================================

-----------------------------
PASSO 1 – DESCOMPACTAR O ARQUIVO
-----------------------------

1. Extraia o arquivo ZIP em uma pasta do seu computador.
2. Abra a pasta extraída.
3. Verifique se dentro dela existe a pasta:
   00. APP HFACS-ACCIMAPS

-----------------------------
PASSO 2 – CRIAR CONTA NO GITHUB
-----------------------------

1. Entre no site do GitHub.
2. Crie sua conta, caso ainda não tenha.
3. Depois de entrar, clique em "New repository".
4. Dê um nome simples ao repositório.
   Exemplo:
   co-safe-ai
5. Deixe como Public.
   Isso é o mais simples para publicar no Streamlit Cloud.
6. Clique em Create repository.

-----------------------------
PASSO 3 – ENVIAR OS ARQUIVOS PARA O GITHUB
-----------------------------

JEITO MAIS SIMPLES PARA LEIGO:

1. Abra o repositório recém-criado no GitHub.
2. Clique em "Add file".
3. Clique em "Upload files".
4. Arraste a pasta inteira "00. APP HFACS-ACCIMAPS" para a tela.
   Se o GitHub não aceitar a pasta inteira de uma vez, entre na pasta e arraste todos os arquivos e subpastas.
5. Aguarde o upload terminar.
6. Embaixo, clique em "Commit changes".

IMPORTANTE:
Se o GitHub reclamar do tamanho de algum arquivo, o mais provável é que seja o vídeo da pasta 03. Teste.
Nesse caso:
- não envie a pasta 03. Teste
- ou apague apenas o vídeo antes do upload

O app não precisa do vídeo para funcionar.

-----------------------------
PASSO 4 – CRIAR CONTA NO STREAMLIT COMMUNITY CLOUD
-----------------------------

1. Entre no site do Streamlit Community Cloud.
2. Faça login com sua conta GitHub.
3. Autorize o acesso ao GitHub quando for solicitado.

-----------------------------
PASSO 5 – PUBLICAR O APP
-----------------------------

1. Dentro do Streamlit Cloud, clique em "New app".
2. Escolha o repositório que você criou no GitHub.
3. Escolha a branch principal.
   Normalmente: main
4. No campo Main file path, coloque exatamente:

00. APP HFACS-ACCIMAPS/01. APP/app.py

5. Clique em Deploy.

Neste momento o app vai tentar abrir.
Mas provavelmente ainda vai faltar a chave da OpenAI.

-----------------------------
PASSO 6 – ADICIONAR A CHAVE DA OPENAI
-----------------------------

1. No Streamlit Cloud, abra o app publicado.
2. Clique no menu do app.
3. Vá em Settings.
4. Abra a área Secrets.
5. Cole exatamente neste formato:

OPENAI_API_KEY = "SUA_CHAVE_AQUI"

Exemplo:
OPENAI_API_KEY = "sk-xxxxxxxxxxxxxxxx"

6. Salve.
7. Reinicie o app, se necessário.

Pronto.
Seu app deverá funcionar pela internet.

============================================================
5. COMO SABER SE DEU CERTO
============================================================

Se tudo estiver certo:
- o app abrirá no navegador
- as imagens/logos aparecerão
- o botão "Gerar relatórios com IA" funcionará
- a leitura dos PDFs de suporte será carregada automaticamente

============================================================
6. LINK PARA ACESSAR DE QUALQUER COMPUTADOR
============================================================

Depois de publicado, o Streamlit gera um link.
Exemplo:
https://seu-app.streamlit.app

Esse link poderá ser aberto em qualquer computador com internet.

============================================================
7. COMO ATUALIZAR O APP NO FUTURO
============================================================

Sempre que você quiser mudar algo:

1. Edite os arquivos no seu computador
2. Envie os arquivos atualizados para o mesmo repositório do GitHub
3. O Streamlit normalmente atualiza sozinho
4. Se não atualizar, abra o app no Streamlit Cloud e clique em Reboot ou Restart

============================================================
8. PROBLEMAS COMUNS E SOLUÇÕES
============================================================

PROBLEMA 1: "OPENAI_API_KEY não configurada"
Solução:
- Vá em Settings > Secrets no Streamlit Cloud
- Cole a chave corretamente

PROBLEMA 2: As imagens não aparecem
Solução:
- Confirme se a pasta "02. Figuras e Layout" foi enviada ao GitHub

PROBLEMA 3: Os PDFs de suporte não são lidos
Solução:
- Confirme se a pasta "00. Suporte ao APP" foi enviada ao GitHub
- Confirme se os PDFs estão dentro dela

PROBLEMA 4: Erro por arquivo muito grande no GitHub
Solução:
- remova o vídeo da pasta 03. Teste
- o vídeo não é necessário para o funcionamento do app

PROBLEMA 5: O app abre, mas a IA não responde
Solução:
- confira se a chave da OpenAI é válida
- confira se há crédito/uso disponível na conta da API

============================================================
9. RECOMENDAÇÃO IMPORTANTE
============================================================

Para simplificar ainda mais, você pode remover a pasta:
03. Teste

Ela não é necessária para rodar o app online.
Isso deixa o upload mais leve.

============================================================
10. RESUMO BEM CURTO
============================================================

Faça nesta ordem:

1. Extraia o ZIP
2. Crie um repositório no GitHub
3. Envie a pasta do projeto para o GitHub
4. Entre no Streamlit Cloud
5. Clique em New app
6. Escolha o repositório
7. Informe o caminho:
   00. APP HFACS-ACCIMAPS/01. APP/app.py
8. Em Settings > Secrets, cole:
   OPENAI_API_KEY = "SUA_CHAVE"
9. Salve
10. Use o link do app em qualquer computador

