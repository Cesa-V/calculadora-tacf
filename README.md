# Calculadora TACF

Simulador responsivo do **Teste de Avaliação do Condicionamento Físico (TACF)**, baseado nas tabelas dos **Anexos IV, V e VI da NSCA 54-3** disponibilizadas como referência para este projeto.

## Funcionalidades

- Perfil por sexo, idade e estatura.
- Circunferência da cintura, flexões e abdominais.
- Corrida/marcha de 12 minutos ou caminhada substitutiva de 4,8 km.
- Pontuação por OIC e soma total (0 a 100 pontos).
- Conceituação por prova e conceito global (I, S, B, MB, E).
- Indicação de suficiência individual, metas para o próximo conceito e cópia do resultado.
- Interface para celular ou computador; PWA instalável, com acesso offline depois da primeira visita.

**Nota importante:** o aplicativo é **não oficial** e não substitui a avaliação regulamentar. A nota global não corrige uma insuficiência individual. A caminhada substitutiva depende das condições e da decisão do avaliador previstas no Anexo V, não sendo livre escolha do avaliado.

### Critério para valores entre linhas da tabela

Para evitar atribuir pontuação superior à marca registrada, a consulta usa a marca imediatamente inferior para a corrida (incrementos de 10 m), superior para a cintura (incrementos de 0,5 cm) e tempo imediatamente mais lento para a caminhada. Não se interpola a nota entre linhas. A suficiência individual usa diretamente os limites do Anexo IV e do Anexo V.

## Arquivos

```text
calculadora-tacf/
├── index.html           # Interface, estilos, tabelas e lógica de cálculo
├── manifest.webmanifest # Configuração de instalação como PWA
├── sw.js                # Armazenamento offline e atualização online
├── icon-192.png         # Ícone do aplicativo
├── icon-512.png         # Ícone do aplicativo
├── .nojekyll            # Evita processamento desnecessário pelo Jekyll
└── README.md            # Documentação
```

## Publicar no GitHub Pages (sem terminal)

1. Crie um repositório no GitHub, por exemplo **calculadora-tacf**.
2. Clique em **Add file → Upload files**.
3. Envie os arquivos desta pasta para a **raiz** do repositório (não envie apenas o `.zip` nem uma pasta contendo os arquivos).
4. Clique em **Commit changes**.
5. Entre em **Settings → Pages**.
6. Em **Build and deployment → Source**, selecione **Deploy from a branch**.
7. Selecione **main** e **/(root)**; clique em **Save**.
8. Após a publicação, acesse: `https://SEU-USUARIO.github.io/calculadora-tacf/` (substitua o usuário e, se necessário, o nome do repositório).

Se o repositório tiver outro nome, a URL termina com o nome correspondente. As alterações futuras em `main` serão publicadas automaticamente.

## Publicar pelo terminal

No diretório que contém estes arquivos:

```bash
git init
git add .
git commit -m "Versão inicial da calculadora TACF"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/calculadora-tacf.git
git push -u origin main
```

Crie o repositório vazio no GitHub antes do `push` e ajuste `SEU-USUARIO`.

## Executar localmente

Abra `index.html` no navegador. Para testar a instalação PWA e o service worker, sirva a pasta com HTTP local:

```bash
python -m http.server 8000
```

Depois abra `http://localhost:8000/`.

## Base normativa

- **Anexo IV:** apreciação de suficiência por sexo e faixa etária/estatura e conceito global.
- **Anexo V:** prova substitutiva da capacidade aeróbica.
- **Anexo VI:** pontuação de cada OIC por sexo e faixa etária/estatura.

Os valores precisam ser conferidos com a edição normativa aplicável antes de uso institucional ou em avaliação oficial.
