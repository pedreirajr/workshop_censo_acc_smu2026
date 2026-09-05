# Dados Censitários e Acessibilidade Urbana em R

Material prático da oficina **Dados Censitários e Acessibilidade Urbana em R**, oferecida no
**Simpósio de Mobilidade Urbana — Modelagem de Tráfego para Cidades Inteligentes e Conectadas**
(EESC-USP, São Carlos-SP, 8 a 11 de setembro de 2026).

📖 **Site da oficina:** <https://pedreirajr.github.io/workshop_censo_acc_smu2026/>

## Instrutores

- Jorge Ubirajara Pedreira Junior
- Thiago Louro
- Lucas Assis

## Conteúdo

A oficina tem 8 horas, divididas em 4 horas de dados censitários e 4 horas de acessibilidade
urbana, com 2 horas expositivas e 2 horas práticas em cada bloco. Este repositório contém apenas o
material das partes práticas.

**Parte 1 — Dados censitários**

1. Instalação e ajustes iniciais
2. Recortes territoriais
3. Agregados por setor censitário
4. Microdados da amostra
5. CNEFE
6. Grade estatística

**Parte 2 — Acessibilidade urbana**

7. Instalação e ajustes iniciais
8. Leitura dos arquivos e montagem da rede
9. Cômputo dos indicadores
10. Equidade e pobreza de acessibilidade

Todas as aplicações usam **Anápolis-GO** como estudo de caso.

## Dados

Os arquivos que não são produzidos por código estão no *release*
[`dados`](https://github.com/pedreirajr/workshop_censo_acc_smu2026/releases/tag/dados) e são
baixados pelo próprio código dos capítulos para a pasta `dados/`, que não é versionada.

```
dados/
├── censo/   agregados, microdados e CNEFE de Anápolis
├── geo/     grade hexagonal H3 e rede de links do modelo de tráfego (Visum)
└── r5/      rede viária (.pbf), GTFS (.zip) e relevo (.tif)
```

Os demais dados do Censo são obtidos ao vivo pelos pacotes `censobr` e `geobr`.

## Como renderizar localmente

Requer [Quarto](https://quarto.org) e R.

```bash
quarto render          # site completo, gerado em docs/
quarto preview         # preview com recarga automática
quarto render 3-agregados.qmd   # um capítulo específico
```

O site é publicado pelo GitHub Pages a partir da pasta `docs/` da branch `main`.
