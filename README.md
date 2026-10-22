# Calculadora TACF — versão 2.0.0

Ferramenta **independente, não oficial**, de simulação do Teste de Avaliação do Condicionamento Físico.

## Funcionalidades

- Calculadora de pontuação e suficiência por OIC, conforme o arquivo de anexos fornecido.
- Consulta completa aos índices de suficiência e pontos por sexo/faixa etária/estatura.
- Planejador da corrida de 12 minutos: distância-alvo para S/B/MB/E, margem opcional, pace, velocidade, voltas de 400 m e parciais de 200 m; conversão de pace para distância estimada.
- Metas globais (20/40/70/90 pontos), diagnóstico individual e indicação de próximos limites.
- Histórico salvo apenas no armazenamento do navegador, recuperação e exclusão das simulações, compartilhamento por texto.
- Interface responsiva inspirada em azuis da FAB, sem utilizar brasões oficiais.
- Instalação PWA e uso offline após primeira visita.

## Base normativa e importante limitação

Pontuações e limites vêm dos **Anexos IV, V e VI do arquivo disponibilizado**. O arquivo começa no Anexo IV, sem capa/portaria, de modo que **a edição exata dele não pode ser afirmada**. Em 2026, houve reedição oficial da **NSCA 54-3 pela Portaria CDA nº 28/SCMD, de 25 de abril de 2026**. Este software **ainda não foi integralmente comparado** com a edição de 2026. Veja a reedição no [SISLAER da FAB](https://www.sislaer.fab.mil.br/TerminalWebCENDOC/VisualizadorPdf?codigoArquivo=47976&tipoMidia=0).

As notas de dados intermediários usam consulta conservadora, uma convenção informativa de software. A caminhada substitutiva depende de decisão do avaliador e requisitos médicos; não é livre escolha do militar. Use a norma vigente para fins oficiais.

## Publicar gratuitamente no GitHub Pages

1. Crie um repositório, como `calculadora-tacf`.
2. Extraia o ZIP e faça upload de **todos os arquivos da pasta** para a raiz do repositório, em **Add file → Upload files → Commit changes**.
3. Em **Settings → Pages**, selecione **Deploy from a branch**, depois **main** e **/(root)**.
4. Acesse `https://SEU-USUARIO.github.io/calculadora-tacf/`.

## Executar localmente

Abra `index.html` ou rode `python -m http.server 8000` na pasta e acesse http://localhost:8000. O PWA depende de HTTPS ou localhost.

## Estrutura

`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `.nojekyll`, `README.md`.
