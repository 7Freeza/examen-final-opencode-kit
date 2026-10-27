# Examen final — OpenCode Kit

Dos ZIP separados para preparar Ubuntu y dejar a OpenCode trabajando con reglas claras.

## 1. `opencode_install_ubuntu.zip`

Contiene **solo**:

```text
INSTALAR_OPENCODE_UBUNTU.txt
```

Pasos:

1. Descargar y extraer.
2. Abrir el TXT.
3. Ejecutar los comandos en Ubuntu.
4. Verificar:

```bash
opencode --version
```

5. Conectar la API:

```bash
opencode
```

Dentro de la TUI:

```text
/connect
```

## 2. `opencode_exam_agent.zip`

Contiene:

```text
LEEME.txt
INSTRUCCIONES.md
AGENTS.md
SKILL.md
```

Pasos:

1. Descargar y extraer en una carpeta.
2. Abrir OpenCode dentro del proyecto del examen.
3. Decirle:

```text
Leé INSTRUCCIONES.md de la carpeta <ruta> y ejecutá todo lo que dice.
Primero revisá el entorno y pedime el PDF del examen.
```

OpenCode debe:

- revisar Docker, Python, Node, Git y dependencias;
- instalar lo que falte si tiene permisos;
- copiar `AGENTS.md` al proyecto;
- instalar `SKILL.md` en `~/.config/opencode/skills/examen-arquitectura/`;
- pedir el PDF;
- leerlo y decidir Lambda o Medallion;
- construir, probar y explicar.

## Importante

- OpenCode **no lee ZIP directamente**: hay que extraerlo.
- No hay API keys ni secretos en este repo.
- La decisión de arquitectura se toma después de leer el PDF.
- Recomendación por defecto: **Lambda** si hay histórico + tiempo real + reconciliación.
- Si el PDF es batch-only, Medallion puede ser suficiente.
