# AAMG CLUB — Aplicação web própria

Este é o **frontend React + Vite** da AAMG CLUB. Projeto independente em arquivos e dependências do antigo Payload Training App.

## Rodar e publicar
- **Node.js 22+**
- `npm install`
- `npm run dev` para desenvolvimento
- `npm run build` para gerar a pasta `dist`
- Hospedagem estática: build `npm ci && npm run build`, diretório publicado `dist`

## Organização
- `src/main.jsx`: telas e regras da demonstração (a modularizar antes da produção)
- `src/styles.css`: estilos e responsividade
- `public/aamg-logo.svg`: marca apresentada no aplicativo
- `index.html`: entrada do aplicativo

## Segurança e limitações
**Esta versão é uma demonstração pública. Não inserir dados pessoais reais, avaliações ou prescrições clínicas.** Os dados são gravados no localStorage de cada navegador; não existe autenticação, servidor nem sincronização. Qualquer pessoa que acesse o site pode visualizar os alunos fictícios. Os dados locais podem desaparecer se o navegador for limpo, e não substituem backups.

O login real e o isolamento de informações por aluno devem ser implementados em backend com autenticação e autorização no banco (ex.: Supabase com RLS). **Nunca incluir segredos de servidor, senhas ou service_role key em arquivos do frontend**.

## Recuperação e manutenção assistida por IA
1. No GitHub, abra a aba de commits para ver a última alteração. Solicite à IA que compare o commit com a versão anterior antes de editar.
2. Para uma correção, crie uma branch de trabalho. Faça build e teste no ambiente de demonstração.
3. Publique somente quando a aplicação compilar e os fluxos críticos forem verificados; mantenha uma versão estável para reversão.
4. Se um deploy novo falhar, escolha no Render a última publicação bem-sucedida para reimplantar.
5. Para resetar **somente dados demonstrativos** em um navegador, use “Restaurar exemplo” na interface. Isso não restaura dados de produção.
6. Antes de introduzir banco de dados real, implemente backup/exportação automatizados e testes de permissões.

## Transferência para repositório próprio
Crie no GitHub um repositório **privado** chamado `aamg-club-app`, vazio e sem inicialização automática (sem README). Depois mova para ele **somente os arquivos desta branch**, sem herdar o histórico ou os arquivos antigos. Reconfigure no Render a origem desse novo repositório e confirme o deploy antes de encerrar a origem anterior.

## Próximos passos técnicos
- Separar `src/main.jsx` em componentes e módulos.
- Criar testes para modelos, superséries, filtros e cálculo de volume.
- Substituir localStorage por armazenamento seguro com controle de acesso.
- Exibir nome e identificador de release na interface para facilitar suporte.
