# 📋 Monitoria – Controle de Plantões e Atendimentos

Sistema web para registro de atendimentos em monitoria/plantão acadêmico, com armazenamento local, relatórios mensais e exportação para Excel (CSV) e PDF.

## 🎯 Funcionalidades

- ✅ Registrar atendimentos por **mês** (selecionar mês/ano)
- ✅ Informar quantos **dias de plantão** houve no mês
- ✅ Adicionar múltiplos **alunos** com:
  - Nome completo
  - Matrícula
  - **Data do atendimento** (opcional)
  - Quantas vezes buscou auxílio no mês
- ✅ Salvar os dados no **localStorage** do navegador (permanecem mesmo após fechar a página)
- ✅ Carregar, visualizar e excluir registros de meses anteriores
- ✅ Gerar **relatório completo** (todos os meses) em:
  - **CSV** (abre no Excel, Google Sheets, etc.)
  - **PDF** (via impressão do navegador)
- ✅ Gerar **PDF apenas do mês atual**
- ✅ **Resumo por aluno (acumulado)**:
  - Total de atendimentos (soma de vezes)
  - Total de dias de plantão nos meses em que apareceu
  - Detalhamento por mês com dias, vezes e data
- ✅ Layout responsivo (funciona no celular, tablet e desktop)

## 🚀 Como usar (GitHub Pages)

1. Faça o download do arquivo `index.html` (ou copie o código completo).
2. Crie um repositório no GitHub.
3. Faça o upload do arquivo `index.html` para o repositório.
4. Vá em **Settings > Pages** e selecione a branch principal como fonte (ex: `main`).
5. O site estará disponível em `https://SEU_USUARIO.github.io/REPOSITORIO/`.

> 💡 Nenhuma configuração adicional é necessária – tudo roda no navegador.

## 📂 Estrutura dos dados (localStorage)

Os registros são salvos na chave `monitoria_plantoes`. Exemplo de estrutura:

```json
{
  "2025-03": {
    "dias": 8,
    "students": [
      { "nome": "João Silva", "matricula": "2024001", "vezes": 3, "data": "2025-03-15" }
    ]
  }
}
