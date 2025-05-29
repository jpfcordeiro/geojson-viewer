# Visualizador GeoJSON Interativo

Uma aplicação web simples e interativa para carregar, visualizar, estilizar e exportar dados GeoJSON em um mapa dinâmico.

## Funcionalidades Implementadas

* **Carregamento de Dados GeoJSON:**
    * Carregar arquivos GeoJSON (`.geojson`, `.json`) do computador local.
    * Inserir ou colar dados GeoJSON diretamente em uma área de texto com syntax highlighting (JSON).
* **Visualização no Mapa:**
    * Renderização de feições GeoJSON (Pontos, Linhas, Polígonos, MultiPontos, etc.) em um mapa interativo fornecido pelo Leaflet.js.
    * Pop-ups interativos ao clicar em feições, exibindo suas propriedades.
    * Ajuste automático do zoom do mapa para exibir completamente os dados carregados.
* **Estilização Dinâmica:**
    * Controles para personalizar a aparência das feições GeoJSON:
        * **Linhas/Bordas:** Cor, espessura e opacidade.
        * **Preenchimento (Polígonos):** Cor e opacidade.
        * **Pontos (renderizados como círculos):** Cor e raio.
    * Aplicação imediata dos estilos na camada GeoJSON ativa.
    * Os estilos definidos são aplicados a novos dados carregados.
* **Exportação de Dados:**
    * **Exportar como GeoJSON:** Baixar os dados GeoJSON atualmente carregados na camada do mapa (ou do editor de texto, se a camada estiver vazia) como um arquivo `.geojson` formatado.
    * **Exportar Mapa como Imagem:** Baixar a visualização atual do mapa como um arquivo de imagem PNG.
* **Interface do Usuário:**
    * Layout responsivo dividido em:
        * Painel de Controles (carregar arquivo, estilização, exportação).
        * Área do Mapa.
        * Painel de Entrada de Texto GeoJSON com editor CodeMirror.
    * Cabeçalho com o título da aplicação.

## Tecnologias Utilizadas

* **Frontend:**
    * HTML5
    * CSS3
    * JavaScript (ES6+)
* **Bibliotecas JavaScript:**
    * **Leaflet.js (v1.9.4):** Para mapas interativos.
    * **CodeMirror (v5.65.15):** Para o editor de texto com syntax highlighting para JSON.
    * **leaflet-image (v0.4.0):** Para exportar o mapa Leaflet como uma imagem.

## Como Executar Localmente

1.  **Baixar os arquivos:**
    * Faça o download ou clone este repositório para o seu computador.
    * Certifique-se de que os seguintes arquivos estejam na mesma pasta:
        * `index.html`
        * `style.css`
        * `app.js`

2.  **Abrir no Navegador:**
    * Abra o arquivo `index.html` em qualquer navegador web moderno (como Chrome, Firefox, Edge, Safari).

    Não é necessário nenhum servidor web ou processo de compilação para esta aplicação, pois ela é puramente client-side.

## Como Usar a Aplicação

1.  **Carregar Dados GeoJSON:**
    * **Via Arquivo:** Na seção "Controles" à esquerda, clique em "Carregar GeoJSON (arquivo)", procure e selecione um arquivo `.geojson` ou `.json` do seu computador. Os dados serão exibidos no mapa.
    * **Via Texto:** Na seção à direita "Inserir GeoJSON (texto)", cole seu código GeoJSON na área de texto (que possui syntax highlighting). Clique no botão "Renderizar do Texto". Um GeoJSON de exemplo é carregado inicialmente nesta área.
2.  **Interagir com o Mapa:**
    * Use o mouse para arrastar (pan) e a roda do mouse (ou botões +/- do Leaflet) para aplicar zoom.
    * Clique em qualquer feição no mapa para ver suas propriedades em um pop-up.
3.  **Estilizar as Feições:**
    * No painel "Controles", use as opções sob "Estilo do GeoJSON" (seletores de cor, sliders de intervalo para espessura, opacidade, raio) para definir a aparência desejada.
    * Clique no botão "Aplicar Estilo" para que as mudanças sejam refletidas na camada GeoJSON atualmente visível.
    * Qualquer novo GeoJSON carregado subsequentemente também usará esses estilos.
4.  **Exportar Dados:**
    * **Para GeoJSON:** Clique no botão "Exportar como GeoJSON". Um arquivo chamado `mapa_exportado.geojson` (ou `editor_exportado.geojson`) será baixado.
    * **Para Imagem:** Clique no botão "Exportar Mapa como PNG". Uma imagem `mapa_exportado.png` da visualização atual do mapa será baixada.

## Funcionalidades Futuras

* Ferramentas de desenho para criar e editar feições GeoJSON diretamente no mapa (pontos, linhas, polígonos).
* Suporte para exportação para outros formatos vetoriais (ex: Shapefile, KML), o que pode requerer bibliotecas adicionais ou processamento no lado do servidor.
* Mais opções de estilização avançada (ex: ícones personalizados para pontos, padrões de preenchimento, rótulos).
* Capacidade de carregar GeoJSON a partir de uma URL.
* Visualização e edição de atributos das feições em uma interface de tabela.
* Gerenciamento de múltiplas camadas.