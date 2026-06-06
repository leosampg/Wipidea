# Wipidea

Funil visual para capturar, resfriar, avaliar e executar ideias — para empreendedores e mentes criativas.

## Como usar

Abra **`index.html`** com dois cliques (Chrome, Edge, Firefox...). Não precisa instalar nada, nem internet, nem servidor. Os dados ficam salvos no próprio navegador (LocalStorage).

## Atalhos

| Tecla | Ação |
|-------|------|
| `N`   | Nova ideia (captura rápida) |
| `/`   | Focar na busca |
| `Esc` | Fechar janela aberta |
| `Ctrl/Cmd + Enter` | Salvar a captura |

## Fluxo (o funil)

1. **Quarentena** — toda ideia nova "esfria" aqui. Fica travada (não avança) por **48h** para evitar decisão no impulso. O anel mostra o progresso e quanto falta.
2. **Em Avaliação** — ao mover para cá, abre a matriz de pontuação (3 critérios de 1 a 5).
3. **Executar** — ideias prioritárias. Abrem o **Canvas do MVP** (dor/público, teste de 30 dias, métricas).
4. **Incubar** — boas, mas sem timing.
5. **Arquivadas** — histórico de descartadas.

Arraste os cards entre colunas, ou use **"Mover para"** dentro do card (útil no celular).

## Como o Score é calculado

Score = **média geométrica** dos três fatores: `∛(alinhamento × viabilidade × impacto)`, na escala 1–5.

Escolhi média geométrica em vez de média simples ou multiplicação porque:
- **Fica legível** (sempre /5), diferente da multiplicação pura (1–125).
- **Pune o elo fraco**: uma ideia 5/5/1 cai para **2.9** — não passa por "boa" só porque acerta em duas dimensões. É exatamente o que um funil de filtragem precisa.

Faixas: **≥ 3.75** prioridade alta · **2.5–3.7** média · **< 2.5** repensar.

## Configurações (ícone de engrenagem)

- Alternar tema (Escuro / Claro).
- Ajustar o tempo de resfriamento (padrão 48h; use `0` para desativar em testes).
- **Exportar / Importar** backup `.json` dos seus dados.

## Stack

Um único arquivo HTML — JavaScript puro, drag-and-drop com Pointer Events + animação FLIP, sem dependências externas.
