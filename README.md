# Minhas Finanças

Aplicativo web de gestão financeira pessoal, responsivo e em pt-BR.

## Stack
- React + TypeScript + Vite
- Tailwind CSS
- Supabase Auth + PostgreSQL (migração incluída)
- Recharts para gráficos
- Lucide para ícones

## Desenvolvimento
```bash
npm install
cp .env.example .env
npm run dev
```

Configure `VITE_SUPABASE_URL` e `VITE_SUPABASE_ANON_KEY` no arquivo `.env`. Sem essas variáveis, o app abre em modo local de demonstração usando localStorage; não use esse modo para dados reais multiusuário.

## Banco de dados
Execute `supabase/migrations/001_initial_schema.sql` no projeto Supabase. As tabelas usam RLS e políticas por `auth.uid()`.

## Observação
O primeiro commit inicializa o repositório. Antes de usar em produção, configure Supabase, valide as políticas no seu projeto e publique após testes.
