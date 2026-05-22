# Dashboard Início do Dia

## Sobre o Projeto
Uma aplicação web leve e moderna em página única (SPA) que atua como um painel pessoal para organizar o início do seu dia de trabalho. A aplicação integra-se aos serviços do Google para trazer um resumo rápido sobre a quantidade de e-mails não lidos, suas próximas reuniões agendadas, além de apresentar indicadores e gráficos interativos de forma elegante e centralizada.

## Funcionalidades
- **Autenticação com o Google**: Login prático e seguro utilizando os serviços de identidade do Google (OAuth 2.0).
- **Caixa de Entrada**: Integração com a API do Gmail para contabilizar em tempo real seus e-mails não lidos na caixa de entrada.
- **Agenda do Dia**: Integração com a API do Google Calendar para listar e contabilizar as reuniões marcadas para a data atual.
- **Gráfico de Interações**: Um gráfico em barras responsivo e estilizado (utilizando [Chart.js](https://www.chartjs.org/)) que ilustra o volume de e-mails na semana (com dados de demonstração).
- **Interface Moderna (UI/UX)**: 
  - Design premium com tema escuro (Dark Mode).
  - Tipografia suave utilizando a família 'Outfit' (Google Fonts).
  - Layout totalmente responsivo para desktop e dispositivos móveis (CSS Grid e Flexbox).
  - Micro-animações e efeitos de hover para melhor usabilidade.

## Tecnologias Utilizadas
- **Frontend**: HTML5, CSS3 (Vanilla, variáveis nativas, pseudo-elementos e keyframes), e JavaScript (Vanilla).
- **Bibliotecas e APIs**:
  - `gapi` (Google API Client Library) e Google Identity Services para autenticação e consumo de dados.
  - APIs de leitura do Gmail (`gmail.readonly`) e do Google Calendar (`calendar.readonly`).
  - `Chart.js` (via CDN) para renderização do gráfico analítico.

## Pré-requisitos e Execução
Como o projeto é construído em um único arquivo estático `index.html`, executá-lo é muito simples, mas requer o uso de um servidor local para que o fluxo de autenticação do Google funcione corretamente (evitando bloqueios do navegador por abrir diretamente usando o protocolo `file://`).

1. Clone ou baixe este repositório para o seu computador.
2. Abra a pasta do projeto em seu terminal.
3. Inicie um servidor web local. Se estiver usando o VS Code, você pode usar a extensão **Live Server**. Como alternativa, use o Python ou Node.js:
   - Com Python: `python -m http.server 8000`
   - Com Node.js (npx): `npx serve .`
4. Acesse o endereço disponibilizado (ex: `http://localhost:8000`) no seu navegador.
5. Clique em **"Entrar com Google"**, conceda as permissões de leitura de E-mail e Agenda e visualize o seu painel atualizado.

> **Importante:** O projeto utiliza um `CLIENT_ID` do Google Cloud Console (`500018491278-ntjqsf2ati3el1c14gjrpfcg2fotigu6.apps.googleusercontent.com`). Para que a autenticação seja permitida, o domínio ou a porta `localhost` em que você está rodando precisa estar cadastrada nas origens permitidas da credencial no Google Cloud. 

## Estrutura de Arquivos
- `index.html`: Arquivo central do projeto. Contém as tags HTML, os estilos visuais na seção `<style>`, e os scripts de inicialização, configuração da API do Google, tratamento do Login e manipulação da interface na seção `<script>`.
- `.git`: Controle de versionamento do projeto.
