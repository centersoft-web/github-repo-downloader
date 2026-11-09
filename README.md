# GitHub Repo Downloader

Aplicação web para pesquisar, selecionar e baixar repositórios públicos do GitHub diretamente pelo navegador.

O projeto foi desenvolvido com HTML, CSS e JavaScript e funciona sem backend. A interface permite localizar os repositórios de um usuário, acompanhar o progresso e escolher entre downloads separados ou a criação de um arquivo ZIP único.

## Funcionalidades

- Consulta de repositórios públicos por nome de usuário do GitHub.
- Exibição do avatar, nome, usuário e biografia do perfil.
- Pesquisa instantânea por nome, descrição ou linguagem.
- Contador de repositórios carregados, visíveis e selecionados.
- Seleção individual de repositórios.
- Opções para marcar os repositórios visíveis ou desmarcar todos.
- Barra de progresso individual para cada repositório.
- Barra de progresso geral da operação.
- Download separado dos repositórios selecionados.
- Botão adicional para criar um ZIP único com os repositórios selecionados.
- Layout responsivo para computadores, celulares e tablets.

## Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- API REST do GitHub
- JSZip

## Como usar

1. Abra o arquivo `github-repo-downloader-v4-corrigido.html` em um navegador moderno.
2. Digite o nome de usuário do GitHub.
3. Clique em **Listar repositórios**.
4. Utilize a pesquisa instantânea para filtrar os projetos, se necessário.
5. Marque os repositórios desejados.
6. Escolha uma das opções:
   - **Baixar separados:** solicita o download individual de cada repositório.
   - **Criar ZIP único com os selecionados:** reúne os arquivos dos projetos em um pacote único.

## Limitações importantes

- A versão atual consulta somente repositórios públicos.
- Os arquivos baixados representam o conteúdo da branch padrão e não incluem o histórico completo do Git.
- A criação do ZIP único acontece na memória do navegador e é mais indicada para repositórios pequenos ou médios.
- Projetos com muitos arquivos devem ser baixados pela opção **Baixar separados**.
- O uso sem autenticação está sujeito aos limites de requisição da API do GitHub.
- É necessário acesso à internet para consultar o GitHub e carregar a biblioteca JSZip utilizada na versão atual.

## Publicação

Para publicar o projeto, envie o arquivo HTML e os demais arquivos do aplicativo para um serviço de hospedagem estática, como GitHub Pages, Azure Static Web Apps ou outro servidor HTTPS.

Para disponibilizar a instalação como PWA, o projeto também deve possuir, no mínimo:

- `manifest.webmanifest`
- `service-worker.js`
- ícones do aplicativo
- registro do service worker no HTML
- publicação em HTTPS

> A versão HTML atual não se torna automaticamente uma PWA apenas por ser publicada. As instruções de instalação abaixo passam a valer quando os arquivos e requisitos de PWA estiverem configurados corretamente.

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

1. Abra o endereço publicado do projeto.
2. Aguarde o carregamento completo da página.
3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
4. Selecione **Instalar aplicativo** ou **Instalar este site como aplicativo**.
5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione **Instalar aplicativo** ou **Adicionar à tela inicial**.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

- A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
- Abrir somente o arquivo `index.html` pelo computador não garante a instalação como PWA.
- O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
- O funcionamento offline depende da configuração do `service-worker.js` e dos arquivos adicionados ao cache.
- Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

## Estrutura recomendada para uma versão PWA

```text
github-repo-downloader/
├── index.html
├── README.md
├── manifest.webmanifest
├── service-worker.js
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Segurança e privacidade

- Não informe tokens ou credenciais em versões do projeto que não tenham sido preparadas para autenticação segura.
- Revise scripts externos antes de publicar o aplicativo.
- Não armazene tokens de acesso diretamente no código-fonte.
- Ao publicar uma versão própria, informe aos usuários quais dados são consultados e processados.

## Licença

Nenhuma licença específica foi definida no arquivo fornecido. Antes de distribuir ou publicar o projeto, inclua uma licença compatível com a finalidade pretendida e verifique as licenças das bibliotecas externas utilizadas.

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.
