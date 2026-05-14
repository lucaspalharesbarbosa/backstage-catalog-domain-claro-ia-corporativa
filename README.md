# Catálogo Backstage — domínio Claro IA Corporativa

Repositório de **entidades do [Software Catalog](https://backstage.io/docs/features/software-catalog/)** do Backstage para o domínio **Claro IA Corporativa** (SUPERAG, insumos para modelos, governança e uso de LLM em contexto corporativo).

## Conteúdo

| Entidade | Arquivo | Descrição resumida |
|----------|---------|--------------------|
| Domain | [`domains/claro-ia-corporativa.yaml`](domains/claro-ia-corporativa.yaml) | Domínio de negócio *Claro IA Corporativa* |
| System | [`systems/superag-intelligence.yaml`](systems/superag-intelligence.yaml) | Sistema *SUPERAG Intelligence* |
| API | [`apis/super-rag-rest-v1.yaml`](apis/super-rag-rest-v1.yaml) | API REST v1 (OpenAPI embutido) — Super RAG |

Proprietário referenciado nas entidades: `group:default/squad-super-rag`.

## Estrutura do repositório

```
domains/     # recursos kind: Domain
systems/     # recursos kind: System
apis/        # recursos kind: API
locations/   # agregação de URLs para importação no catálogo
```

## Uso no Backstage

1. No `app-config.yaml` do seu Backstage, inclua uma entrada em `catalog.locations` apontando para o arquivo de localizações publicado na branch `main`, por exemplo:

   `https://github.com/lucaspalharesbarbosa/backstage-catalog-domain-claro-ia-corporativa/blob/main/locations/github-locations.yaml`

2. Alternativamente, registre cada YAML individualmente; as URLs seguem o mesmo padrão `.../blob/main/<caminho-do-arquivo>.yaml`.

O arquivo [`locations/github-locations.yaml`](locations/github-locations.yaml) declara um recurso `Location` do tipo `url` com todos os *targets* das entidades acima.

## Formato e referências

Os descritores seguem o [formato de entidades do Backstage](https://backstage.io/docs/features/software-catalog/descriptor-format). Para validar localmente, use as ferramentas e o fluxo de CI do seu ambiente Backstage.
