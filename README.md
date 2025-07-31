# Etiquetas de Garantia

Este sistema foi desenvolvido para facilitar a emissão e controle de etiquetas de produtos enviados para garantia.

## 🧩 Objetivo
Permitir ao operador montar uma folha A4 com etiquetas contendo:
- Código do produto
- Descrição (buscada automaticamente do banco)
- Quantidade
- Causa da garantia
- Data e hora da emissão

## 🚀 Funcionalidades
- Busca da descrição pelo código do produto com cache e feedback visual ("Carregando...")
- Preenchimento obrigatório de todos os campos
- Inclusão de múltiplos produtos com visualização em tempo real
- Prevenção de duplicidade: impede que um mesmo produto seja incluído duas vezes
- Impressão com layout A4 e reset automático após a impressão

## 🔒 Validações
- O botão "Incluir Produto" só é ativado quando:
  - O código for numérico e válido
  - A descrição tiver sido retornada da busca (evita incluir "Carregando...")
  - Quantidade e causa estiverem preenchidas
- O botão "Buscar" fica desabilitado durante a consulta
- Se o código não for encontrado, exibe mensagem de erro
- O botão "Imprimir" é habilitado somente quando houver produtos na fila

## 🎨 UI/UX
- Estética com as cores institucionais: Azul #141b4d, Laranja #ff7a15
- Campos e botões desabilitados ficam em cinza (#ccc)
- Animação de carregamento com três pontos no campo descrição
- Etiquetas com logo `logo-rezende.png`

## 🧠 Tecnologias Utilizadas
- HTML, CSS e JavaScript puro
- Google Apps Script com CacheService para resposta mais rápida
- Integração com Google Sheets via Web App

## 🛠️ Requisitos
- A planilha deve estar publicada como Web App com acesso "qualquer pessoa"
- O arquivo da logo deve estar disponível em `img/logo-rezende.png`
- O banco de dados (planilha) deve ter colunas: `codigo` e `descricao`

## 📂 Estrutura esperada
```
- index.html
- code.gs (Apps Script)
- /img/logo-rezende.png
- Planilha do Google
```

## 📞 Suporte
Em caso de dúvidas ou ajustes, entre em contato com o desenvolvedor responsável ou a equipe de TI.
