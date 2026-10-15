# OrgaLume

**Seu dia, mais organizado.** A identidade visual usa a logo fornecida pelo usuário, preservada no arquivo `dist/orgalume-logo.png`.

Organizador pessoal em português, com painel diário, tarefas, agenda semanal, projetos e notas. Primeira versão em HTML, CSS e JavaScript, sem etapa de build e sem instalação de dependências.

## Abrir localmente

Na pasta do projeto:

```sh
python3 -m http.server 4173 --directory dist --bind 127.0.0.1
```

Acesse http://127.0.0.1:4173. Use sempre a mesma origem para acessar os dados armazenados naquele navegador.

## Recursos

- Criar, editar, concluir, reabrir e excluir tarefas; filtrar por área e status.
- Criar e editar compromissos; navegar entre semanas e selecionar uma data.
- Criar projetos e acompanhar a proporção de tarefas concluídas.
- Criar e editar notas; buscar em todas as coleções com Ctrl/Cmd + K.
- Exportar e restaurar backups JSON com validação de formato.
- Dados de demonstração identificados e opção de começar do zero.
- Interface responsiva, controles com nomes acessíveis e suporte a teclado.

## Dados e limites

Os dados ficam no localStorage do navegador, sob a chave `dia-a-dia.v1`, mantida para preservar os registros da primeira versão durante a mudança de nome para OrgaLume. Não há backend, conta, sincronização entre dispositivos nem integração com Gmail, Calendar ou Drive. A primeira visita recebe dados de exemplo, com datas relativas ao dia atual em America/Sao_Paulo. O resumo é calculado a partir dos registros; não usa IA.

Limpar os dados do navegador remove os registros. Use Dados e preferências → Exportar para guardar uma cópia. Um endereço de produção e um endereço local têm armazenamentos diferentes. A publicação do aplicativo não publica o conteúdo do seu localStorage. Backups podem conter informações pessoais: guarde-os fora do repositório.

## Publicação na Vercel

Importe este repositório no painel da Vercel. Framework: Other. Output Directory: `dist`. Não há comando de instalação ou build. `vercel.json` já configura a pasta de saída.

## Arquivos

- `dist/index.html`: estrutura e diálogos.
- `dist/styles.css`: identidade visual e estilos responsivos.
- `dist/app.js`: dados, validação, renderização e interações.
- `dist/vendor/lucide.min.js`: distribuição oficial Lucide 0.468.0 (ISC).
- `vercel.json`: configuração de publicação.

As fontes DM Sans e Manrope são carregadas pelo Google Fonts; fontes sem serifa do sistema servem de fallback. Ícones são servidos localmente.
