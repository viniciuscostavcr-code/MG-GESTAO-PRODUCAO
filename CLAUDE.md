# GestFood — Sistema de Gestão para Alimentação

## Visão geral
Sistema web de gestão para padarias, confeitarias e supermercados.
Desenvolvido para o Supermercado MG e comercializado para outros estabelecimentos.
Responsável: Vinicius (nutricionista e gerente de produção).

## Arquitetura
- HTML puro + JavaScript vanilla (sem frameworks)
- Backend: Supabase (PostgreSQL)
- Hospedagem: GitHub Pages
- Compatível com iPhone/Safari/android (PWA instalável)
- Arquivos únicos HTML — sem build, sem npm no projeto

## Estrutura de arquivos
- GESTFOOD_INDEX.html → Hub principal com sidebar, splash screen e navegação
- DESPERDICIOS_BETA_1.1.html → Registro e dashboard de desperdícios
- PRODUCAO_BETA_1.0.html → Registro e dashboard de produção
- GESTFOOD_CONFIG.html → Catálogo de produtos, setores e responsáveis
- CHECKLIST_PROJECAO.html → Checklist de estoque (em construção)
- manifest.json → PWA para instalação no iPhone
- icon-gestfood*.png → Ícones do app

## Banco de dados — Supabase
- URL: https://rjkseydseuotdkavskss.supabase.co
- Tabelas: produtos, desperdicios, producao, responsaveis
- RLS habilitado com políticas públicas (allow all)
- Catálogo de produtos compartilhado entre todos os apps

## Design system
- Fonte: Plus Jakarta Sans (Google Fonts)
- Verde escuro: #1B4332 (sidebar, splash)
- Verde médio: #2D6A4F (accent principal)
- Verde claro: #EAF4EF (backgrounds suaves)
- KG sempre em vermelho: #C0392B
- UND sempre em laranja: #E67E22
- Background geral: #F7F7F5
- Sidebar: fundo #1B4332, textos brancos
- Topbar: branca com borda verde 3px embaixo

## Status dos módulos
- Hub (INDEX): ✅ Funcional
- Desperdícios: ✅ Funcional com dashboard completo
- Produção: ✅ Funcional
- Config: ✅ Funcional
- Checklist/Projeção: 🚧 Em construção

## Diretrizes para IA
- Nunca misturar KG e UND no mesmo valor ou gráfico
- KG = vermelho (#C0392B), UND = laranja (#E67E22) — sempre
- Manter compatibilidade com iPhone/Safari
- Não usar frameworks, bundlers ou npm no projeto
- Usar confirm() nunca — sempre usar a função confirmar() própria
- Cada app é um arquivo HTML único e autossuficiente
- Produtos carregados do Supabase (tabela produtos, ativo=true)
- Versioning: APPNAME_BETA_X.X.html
