# O que faz um artista ter sucesso?

Projeto de grupo de **Programming for Data Science** · 2026/27 · Grupo XX

| Nome | Número | Frente de trabalho |
|---|---|---|
| _(por preencher)_ | | Limpeza e qualidade |
| | | Análise e visualização |
| | | Scraping |
| | | Coordenadas e mapas |

**Entrega:** 21 de dezembro, 18h00 · **Defesa:** presencial, obrigatória

---

## Como está organizado

```
notebooks/
├── 01_limpeza.ipynb        produz o dataset limpo
├── 02_perguntas.ipynb      responde às perguntas 2, 4 e 5
├── 03_scraping.ipynb       locais e coordenadas da Wikipédia
├── 04_mapas.ipynb          os dois mapas interativos
├── 05_ds_in_action.ipynb   a secção livre
└── GroupXX_PDS_2627.ipynb  o notebook final, montado no fim
data/
├── raw/        o dataset original, nunca alterado
└── processed/  o que cada frente entrega às outras
outputs/        figuras e ficheiros gerados
```

## Quem depende de quem

- O **01** bloqueia tudo. Até `data/processed/artistas_limpo.csv` estar fechado, ninguém produz
  resultados finais.
- O **02** e o **05** leem esse ficheiro.
- O **03** bloqueia o **04**: os mapas leem `data/processed/locais_coordenadas.csv` e nunca correm
  o scraping.

## Regras

1. **Limpar os outputs antes de cada commit** (*Kernel → Restart & Clear Output*).
2. `git pull` antes de começar, `git push` no fim da sessão.
3. Um ficheiro, um dono. Não editar o notebook de outra pessoa.
4. O que é lento corre uma vez e grava em `data/processed/`.
5. A junção final faz-se **uma semana antes** da entrega, e acaba sempre com *Restart & Run All*.
