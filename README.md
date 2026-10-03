# Métodos para ContentFlow

Métodos de código aberto para o [ContentFlow](https://github.com/andremjr/contentflow), sob licença **MIT**. Você pode usar, adaptar, melhorar, distribuir e vender seus derivados, preservando os avisos de licença e autoria.

## Catálogo inicial

Por enquanto, apenas **Gerar Imagens Flow — Assets Visuais**: roteiro → personagens → referências → cenas consistentes → animações, com sete Blocos. Requer ContentFlow 1.3.3, plugins ChatGPT Browser Studio e Google Flow Browser Images, além dos perfis e contas configurados localmente. Consulte a prévia do aplicativo para as dependências de cada Bloco.

Métodos antigos publicados no site anterior não fazem parte deste catálogo. Outros Métodos serão acrescentados pelo mantenedor quando estiverem prontos.

## Usar no aplicativo

Abra **Métodos → Métodos disponíveis → Importar Método**. Confira as dependências, escolha o Canal e os Processos a aplicar e confirme a importação. As versões publicadas não substituem automaticamente suas personalizações. Credenciais, conexões e perfis permanecem locais e precisam de associação explícita.

## Estrutura e publicação

- `methods/`: fontes portáteis dos Métodos.
- `catalog.json`: catálogo consultado pelo aplicativo.
- Releases: arquivos JSON ou pacotes ZIP imutáveis.
- `scripts/package.mjs`: prepara somente o Método escolhido e uma revisão do catálogo.

A versão `3` do envelope é a versão do contrato. A versão editorial `1.0.0`, `1.0.1` etc. é registrada no catálogo e identifica mudanças do Método.

Para publicar: revise o arquivo, instale as dependências com `npm install` e execute `npm run package -- slug-do-metodo 1.0.1`. Crie a release com a tag indicada, envie o pacote e somente depois publique na raiz o catalog.json preparado pelo script. As demais entradas permanecem intactas. Não é necessária uma nova release do aplicativo. Builds e publicação são locais, sem GitHub Actions.

O catálogo está em https://raw.githubusercontent.com/andremjr/methods-contentflow/main/catalog.json.

Veja [LICENSE](LICENSE) e [LICENSING.md](LICENSING.md). A licença dos Métodos não altera a licença do aplicativo ou dos serviços utilizados.
