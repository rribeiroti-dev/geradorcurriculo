# 📄 Gerador de Currículo Profissional (CV Generator PRO)

Um aplicativo da web de página única (Single-Page Application) completamente independente (self-contained) que permite aos usuários gerar currículos profissionais em formato PDF. Sem necessidade de banco de dados, todo o processamento e salvamento é feito diretamente no seu navegador.

## ✨ Funcionalidades Principais

* **100% Client-Side:** Não é necessário nenhum servidor backend (Node.js, PHP, etc.) para funcionar perfeitamente. Toda a renderização acontece no seu próprio navegador de forma rápida e segura.
* **Formulário Passo a Passo (Multi-step):**
    * Dados Pessoais (com upload de foto instantâneo via Base64)
    * Objetivo Profissional
    * Formação Acadêmica
    * Experiência Profissional
    * Habilidades (Tags dinâmicas)
* **Preview em Tempo Real (Live Preview):** O currículo visual à direita da tela é atualizado no exato momento em que você digita as informações.
* **3 Templates Profissionais Exclusivos:**
    1. **Clássico:** Tradicional, fonte serifada, formato de coluna única limpo e ideal para ambientes corporativos formais.
    2. **Moderno:** Formato dinâmico em duas colunas, barra lateral colorida para destaques e foto de perfil perfeitamente enquadrada.
    3. **Criativo:** Cabeçalho robusto com gradientes modernos, divisórias dinâmicas e design arrojado focado em startups e áreas criativas.
* **Sistema de Salvamento Automático (LocalStorage):** Começou a preencher e fechou a guia sem querer? Seus dados estão salvos e persistem no cache do seu navegador para a próxima vez que você abrir a aplicação.
* **Exportação Otimizada para PDF (A4):** Utiliza as poderosas bibliotecas `html2canvas` e `jsPDF` do lado do cliente para entregar um PDF perfeitamente dimensionado na folha A4 com renderização nativa de alta resolução. O download resolve perfeitamente extensões de arquivos em qualquer ambiente (Locais ou via Servidor) devido a um fallback de *Blob URLs*.

## 🛠️ Tecnologias Utilizadas

A grande vantagem deste projeto é não depender de frameworks complexos como React ou Angular. Foi desenvolvido com maestria utilizando:

* **HTML5:** Marcação semântica e acessível.
* **CSS3:** Todo o layout dinâmico responsivo e o grid complexo dos três templates gerados internamente via variáveis nativas.
* **Vanilla JavaScript (ES6+):** Todo o motor de controle de estado e roteamento sem depender do jQuery.
* **jsPDF (v2.5.1):** Biblioteca CDN para a montagem e injeção do arquivo PDF.
* **html2canvas (v1.4.1):** Biblioteca CDN para converter os blocos HTML/CSS de forma idêntica visualmente para uma imagem Canvas de alta densidade antes de injetá-la no PDF.

## 🚀 Como Executar

### Opção 1: Uso Direto (Mais Fácil)
Como toda a arquitetura está contida em apenas um único arquivo, basta você encontrar o arquivo `index.html` na pasta do seu computador e dar um **clique duplo**. Ele será aberto no seu navegador padrão e já estará 100% funcional.

### Opção 2: Servidor de Desenvolvimento Local (Ex: Node.js)
Se você for um desenvolvedor e desejar simular um ambiente de produção ou evitar bloqueios rigorosos de CORS presentes no protocolo `file:///`:

1. Instale o NodeJS na sua máquina.
2. Abra o terminal nesta pasta.
3. Execute o comando de servidor rápido:
   ```bash
   npx serve . -p 3000
   ```
4. Acesse pelo navegador: `http://localhost:3000/`

## 👨‍💻 Fluxo de Edição
Se precisar alterar a estética, cores primárias, as tipografias (*Inter*, *Outfit* e *Lora* do Google Fonts) ou aumentar o limite de caracteres de uma etapa, todo o código-fonte está no único e contido `index.html`. O código possui marcadores e seções bem comentadas (*State Management*, *Preview Engine*, *Storage*, etc.) facilitando qualquer manutenção sem depender de ferramentas de empacotamento (como Webpack ou Vite).
