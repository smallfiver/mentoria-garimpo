# Pacote de Mentoria — Garimpo de Ofertas

Três materiais. Cada um tem uma função diferente — não são versões do mesmo conteúdo.

| Arquivo | Para quem | Quando usar |
|---|---|---|
| **PLAYBOOK.md** | O mentorado lê | Uma vez, antes do primeiro ciclo. É o treinamento. |
| **COMO-USAR.md** | O mentorado consulta | No dia a dia. Comandos, o que esperar, como cobrar. |
| **skill/garimpar-ofertas/** | Instalar no Claude dele | Uma vez. Depois dispara sozinho. |
| **PROMPT-INICIAL.md** | Só se ele não usar Claude Code | Alternativa à skill: colar a cada conversa. |

**Instalando a skill, o PROMPT-INICIAL fica desnecessário** — ela já faz o Claude perguntar
nicho, país, quantidade e formato antes de começar. O prompt existe só para quem usa Claude
sem suporte a skills.

## Como instalar a skill

A skill é melhor que o prompt: uma vez instalada, o Claude dele aciona sozinho quando a
conversa for sobre garimpar oferta — não precisa colar nada.

**Claude Code / Desktop:** copie a pasta `skill/garimpar-ofertas` para dentro de
`.claude/skills/` do projeto dele. Fica assim:

```
<projeto>/.claude/skills/garimpar-ofertas/SKILL.md
```

Reinicie a sessão. Para testar: `garimpa 5 ofertas de emagrecimento no BR`.

**Se ele não usa Claude Code:** o prompt (`PROMPT-INICIAL.md`) faz o mesmo trabalho, só
que precisa ser colado a cada conversa nova.

## Ordem sugerida da mentoria

1. Ele lê o **PLAYBOOK** inteiro.
2. Instala a **skill**.
3. Faz os **4 exercícios** da seção 6 do playbook, nessa ordem.
4. Você revisa a entrega do exercício 3 (ciclo completo) com ele.

O exercício 1 é o mais importante: treina o olho para falso positivo, que é onde quase todo
mundo erra.

## O que o mentorado precisa ter

- Claude com acesso a navegador (para abrir a Biblioteca de Anúncios e as páginas de oferta).
- Nada além disso. Este pacote não depende de banco de dados — a entrega é lista/planilha.

## Nota sobre o que ficou de fora

Este pacote cobre **garimpo puro**: achar, validar e medir oferta, entregando em lista.

Não cobre a parte de operação de SaaS (banco, webhook de pagamento, controle de acesso).
Se um dia o mentorado for mexer nisso, é outro material.
