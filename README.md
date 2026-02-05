# Farmavet Claude Marketplace

Marketplace centralizado de plugins de Claude Code para el equipo Farmavet.

## Plugins Disponibles

| Plugin | Descripción |
|--------|-------------|
| `farmavet-claude-tools` | Task planning and execution with verification-first methodology |

## Configuración

### Agregar este marketplace a Claude Code

```bash
/plugin marketplace add gonzaloramirezabella/mg-claude-marketplace
```

### Instalar un plugin

```bash
/plugin install farmavet-claude-tools@farmavet
```

### Ver plugins disponibles

```bash
/plugin search @farmavet
```

## Auto-configuración en proyectos

Añade a `.claude/settings.json` de tu proyecto:

```json
{
  "marketplaces": [
    {"name": "farmavet-marketplace", "source": {"source": "github", "repo": "gonzaloramirezabella/mg-claude-marketplace"}}
  ],
  "plugins": ["farmavet-claude-tools@farmavet"]
}
```

## Agregar nuevos plugins al marketplace

1. Crea tu plugin siguiendo la estructura estándar (`.claude-plugin/plugin.json`)
2. Sube el plugin a GitHub bajo `github.com/gonzaloramirezabella/`
3. Añade la entrada en `.claude-plugin/marketplace.json` de este repo
4. Crea un MR para revisión

## Estructura de un plugin

```
mi-plugin/
├── .claude-plugin/
│   └── plugin.json      # Metadatos: name, description, version, commands, agents
├── commands/            # Slash commands
│   └── mi-comando.md
└── README.md
```

## Equipo

Mantenido por el equipo de Farmavet.
