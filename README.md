# Dashboard Operacional · Demo

> **Demonstração pública com dados 100% fictícios.** A versão original está em produção para um cliente corporativo do setor de cosméticos, com dados reais e autenticação ativa. Nomes de pessoas, empresas, depoimentos e métricas foram substituídos ou alterados.

🔗 **Demo ao vivo:** https://dashboard-operacoes-demo.vercel.app

## O que é

Dashboard de gestão de operações de aprendizagem corporativa (T&D), construído como **arquivo HTML único** — sem build, sem framework, deploy instantâneo. Acompanha uma operação de facilitação com mais de 1.200 turmas/ano: agenda, capacidade, cronograma de produção, NPS e voz da rede.

## Funcionalidades

- **Autenticação com perfis de acesso** — visão *equipe* (completa) e visão *cliente* (restrita). Em produção usa Supabase Auth + tabela `profiles` com RLS; nesta demo o login é simulado (entre com qualquer e-mail/senha; e-mail contendo `cliente` mostra a visão restrita)
- **Visualizações com Chart.js** — evolução de turmas, capacidade vs. demanda, NPS por ciclo, percepção por categoria
- **Gantt de produção** — cronograma de entregas com perfis (DA/DG), alertas de atraso e gestão de gargalos
- **Filtros estilo Power BI** — toggles combináveis por status, modalidade, público, ciclo e facilitador, com export CSV do recorte filtrado
- **Árvore organizacional interativa** e mapa de atuação com mini-abas
- **Tema claro/escuro**, sidebar colapsável e layout responsivo
- **Camada de dados plugável** — funciona com dados embutidos ou conectada a um Google Sheets publicado em CSV (parser próprio incluído)

## Stack

| Camada | Tecnologia |
|---|---|
| Interface | HTML5, CSS3 (custom properties / design tokens), JavaScript vanilla |
| Gráficos | Chart.js 4 + plugin datalabels |
| Autenticação e dados | Supabase (Auth, Postgres, RLS) — desativado na demo |
| Deploy | GitHub → Vercel (CI/CD) |

## Por que arquivo único?
