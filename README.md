# Agency Hub

Sistema de gestão compartilhada de agência digital.

## Módulos
- Dashboard de clientes, projetos, prazos e receitas
- Kanban de clientes com movimentação entre etapas
- Clientes, serviços avulsos e recorrentes, pagamentos e histórico
- Biblioteca de arquivos por cliente e projeto
- Links úteis por cliente e cofre de credenciais com acesso restrito
- Financeiro: lucro distribuível = receitas efetivamente recebidas - custos operacionais - ferramentas - impostos - terceiros e outras despesas; divisão 50/50; evitar dupla contagem
- Usuários individuais, papéis, trilha de auditoria e backups

## Arquitetura proposta
- Next.js + TypeScript + Tailwind CSS
- Supabase PostgreSQL, Auth, RLS e Storage privado
- Vercel para hospedagem

## Segurança
Nunca registrar senhas de clientes em texto puro no banco, código, logs ou repositório. Usar cofre criptografado com gerenciamento de chaves separado e auditoria de acesso. Todas as tabelas de dados de clientes devem usar políticas RLS. Segredos somente por variáveis de ambiente. Evitar dados reais em seeds.

## Situação
Escopo inicial registrado. Aplicação, migrations, integrações e deploy ainda pendentes.
