# AAMG CLUB — primeira etapa web

Este branch preserva a arquitetura original do Payload Training App e inicia a identidade visual AAMG CLUB na área do aluno.

## Estado
- [x] Branch de trabalho separada da `main`.
- [x] Metadata da área do aluno atualizada para AAMG CLUB.
- [x] Tema claro inicial com tokens azure, branco e verde-piscina.
- [ ] Tradução completa para português brasileiro.
- [ ] Interface administrativa personalizada.
- [ ] Agenda semanal, prescrição e evolução: validar e completar a experiência.
- [ ] Testes de interface e regras de acesso.
- [ ] Publicação em ambiente de testes.

## Executar localmente (Mac, com Docker, Node 24+ e Yarn 4)
```bash
git clone https://github.com/aless-alv/payload-training-app.git
cd payload-training-app
git checkout aamg/primeira-identidade-web
corepack enable
yarn install
cp .env.example .env
```

Inicie um PostgreSQL local, por exemplo com o `docker-compose.yml` do projeto. Configure `DATABASE_URL`, `PAYLOAD_SECRET` (um valor secreto longo e aleatório) e `NEXT_PUBLIC_BASE_URL=http://localhost:3000` no `.env`. **Nunca coloque `.env` no GitHub.** Depois:

```bash
yarn payload migrate
yarn dev
```

Painel do treinador: http://localhost:3000/admin

Área do aluno (idiomas originais, enquanto a tradução não está pronta): http://localhost:3000/pl

O primeiro usuário criado em `/admin` será superadministrador. Dados demonstrativos podem ser criados com `yarn seed` em um banco local de testes.

**Atenção:** a aplicação ainda não foi implantada nem testada em execução neste branch. O CSS inicial precisa de revisão visual em ambiente rodando antes de uso com alunos reais.
