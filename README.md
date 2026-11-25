# Project Continuity

[English](#en) · [Русский](#ru)

<a id="en"></a>

## English

A small set of Markdown instructions for keeping project context between AI agent sessions. I wanted to be able to switch agents or start a new chat without explaining the same project again. The context stays in the workspace, rather than in a particular client. No scripts, databases or Git dependency.

[Installation](#en-setup) · [Usage](#en-usage) · [Project files](#en-files) · [Limitations](#en-limits)

[Codex](#en-codex) · [Claude Code](#en-claude) · [Google Antigravity](#en-antigravity) · [Gemini CLI](#en-gemini) · [Cursor](#en-cursor) · [OpenCode](#en-opencode) · [GitHub Copilot CLI](#en-copilot) · [GitHub Copilot in VS Code](#en-vscode)

<a id="en-setup"></a>

### Installation

Download [AGENTS.md](AGENTS.md) and [handoff/SKILL.md](handoff/SKILL.md). The first contains standing rules; the second describes the save/resume procedure. Copy the **contents** of AGENTS.md into the instruction file for your client (append if it exists), and copy SKILL.md into the indicated skill directory. Create missing directories. Choose either global or project installation; avoid duplicate copies. Start a fresh session in the project root.

Windows paths use `%USERPROFILE%` (Explorer/Win+R); in PowerShell use `$HOME`. For WSL or remote execution, install in the home directory of the environment actually running the agent. Paths below assume default configuration. These are documented discovery locations, not a claim that the workflow has been tested in every client.

<a id="en-codex"></a>

#### Codex

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | `~/.codex/AGENTS.md` | `~/.agents/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.codex\AGENTS.md` | `%USERPROFILE%\.agents\skills\handoff\SKILL.md` |
| Project (all OS) | `AGENTS.md` | `.agents/skills/handoff/SKILL.md` |

Explicit save example: `$handoff save`

[Instructions documentation](https://learn.chatgpt.com/docs/agent-configuration/agents-md) · [Skills documentation](https://learn.chatgpt.com/docs/customization/overview)

[Back to installation](#en-setup)

<a id="en-claude"></a>

#### Claude Code

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | `~/.claude/CLAUDE.md` | `~/.claude/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.claude\CLAUDE.md` | `%USERPROFILE%\.claude\skills\handoff\SKILL.md` |
| Project (all OS) | `CLAUDE.md` | `.claude/skills/handoff/SKILL.md` |

Claude Code uses CLAUDE.md; copying AGENTS.md under its original name alone is not sufficient.

Explicit save example: `/handoff save`

[Instructions documentation](https://code.claude.com/docs/en/memory) · [Skills documentation](https://code.claude.com/docs/en/skills)

[Back to installation](#en-setup)

<a id="en-antigravity"></a>

#### Google Antigravity

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | `~/.gemini/AGENTS.md` | `~/.gemini/config/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.gemini\AGENTS.md` | `%USERPROFILE%\.gemini\config\skills\handoff\SKILL.md` |
| Project (all OS) | `AGENTS.md` | `.agents/skills/handoff/SKILL.md` |

Current App/CLI paths are shown. Older IDE releases may use different directories; check customization discovery in your build.

Explicit save example: `/handoff save`

[Instructions documentation](https://antigravity.google/docs/rules/) · [Skills documentation](https://antigravity.google/docs/skills)

[Back to installation](#en-setup)

<a id="en-gemini"></a>

#### Gemini CLI

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | `~/.gemini/GEMINI.md` | `~/.gemini/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.gemini\GEMINI.md` | `%USERPROFILE%\.gemini\skills\handoff\SKILL.md` |
| Project (all OS) | `GEMINI.md` | `.gemini/skills/handoff/SKILL.md` |

Explicit save example: `Use the handoff skill in SAVE mode.`

[Instructions documentation](https://geminicli.com/docs/cli/gemini-md/) · [Skills documentation](https://geminicli.com/docs/cli/skills/)

[Back to installation](#en-setup)

<a id="en-cursor"></a>

#### Cursor

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | User Rules in settings | `~/.agents/skills/handoff/SKILL.md` |
| Windows | User Rules in settings | `%USERPROFILE%\.agents\skills\handoff\SKILL.md` |
| Project (all OS) | `AGENTS.md` | `.agents/skills/handoff/SKILL.md` |

Explicit save example: `Use the handoff skill in SAVE mode.`

[Instructions documentation](https://cursor.com/docs/rules) · [Skills documentation](https://cursor.com/docs/skills)

[Back to installation](#en-setup)

<a id="en-opencode"></a>

#### OpenCode

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | `~/.config/opencode/AGENTS.md` | `~/.config/opencode/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.config\opencode\AGENTS.md` | `%USERPROFILE%\.config\opencode\skills\handoff\SKILL.md` |
| Project (all OS) | `AGENTS.md` | `.opencode/skills/handoff/SKILL.md` |

The global location follows the client configuration directory; check XDG or custom configuration on your system.

Explicit save example: `Use the handoff skill in SAVE mode.`

[Instructions documentation](https://opencode.ai/docs/instructions/) · [Skills documentation](https://opencode.ai/docs/skills/)

[Back to installation](#en-setup)

<a id="en-copilot"></a>

#### GitHub Copilot CLI

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | `~/.copilot/copilot-instructions.md` | `~/.copilot/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.copilot\copilot-instructions.md` | `%USERPROFILE%\.copilot\skills\handoff\SKILL.md` |
| Project (all OS) | `AGENTS.md` | `.github/skills/handoff/SKILL.md` |

Explicit save example: `Use the handoff skill in SAVE mode.`

[Instructions documentation](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-custom-instructions) · [Skills documentation](https://docs.github.com/en/copilot/reference/customization-cheat-sheet)

[Back to installation](#en-setup)

<a id="en-vscode"></a>

#### GitHub Copilot in VS Code

| Scope | Instructions | Skill |
|---|---|---|
| Linux / macOS | User custom instructions in settings (or use project scope) | `~/.copilot/skills/handoff/SKILL.md` |
| Windows | User custom instructions in settings (or use project scope) | `%USERPROFILE%\.copilot\skills\handoff\SKILL.md` |
| Project (all OS) | `AGENTS.md` | `.github/skills/handoff/SKILL.md` |

Explicit save example: `Use the handoff skill in SAVE mode.`

[Instructions documentation](https://code.visualstudio.com/docs/agents/reference/custom-instructions-reference) · [Skills documentation](https://code.visualstudio.com/docs/agent-customization/agent-skills)

[Back to installation](#en-setup)

<a id="en-usage"></a>

### Usage

Work normally, then send a plain text command to the agent. These are prompts, not shell commands or universally registered slash commands.

| Command | Action |
|---|---|
| `save`, `сохрани` | Save current state |
| `checkpoint`, `чекпоинт` | Save intermediate progress |
| `resume`, `продолжай` | Restore and continue authorized work |

For a quick test, open a temporary workspace, complete a small task and send `save`. Check HANDOFF.md, then open a fresh session and send `resume`. Make another change and save again; verify the previous snapshot was archived. If a client does not load skills, the standing rules include a manual fallback. Any other agent with filesystem access can use the same instructions and read/write the same files.

<a id="en-files"></a>

### Project files

```text
project/
├── HANDOFF.md
└── .handoff/
    ├── DECISIONS.md
    └── history/
        └── YYYY-MM-DDTHH-MM-SSZ-001.md
```

`HANDOFF.md` is the current snapshot: goals, actual progress, constraints, verification, failures, blockers and next steps. `DECISIONS.md` keeps important choices, evidence, alternatives and trade-offs. `history/` preserves previous snapshots; optional detailed notes can live in `.handoff/notes/`. Files are created only when needed. At startup the agent checks the snapshot against actual project state. Important milestones trigger best-effort checkpoints. The workflow also supports research, infrastructure, documents and non-code work.

<a id="en-limits"></a>

### Limitations

This is an instruction-based workflow, not a background service. It cannot guarantee a save after a quota limit, crash or denied write. It does not synchronize machines, lock concurrent writers or automatically commit/push. Use one writer at a time. Snapshots may contain private project details; review them before publication. Do not store credentials. No runtime compatibility tests across clients have been performed. Installation paths were checked against linked documentation on 25 November 2026.

### Credits

Inspired by [thieung/agent-skills](https://github.com/thieung/agent-skills/tree/main/skills/handoff). This version adds decision records, snapshot history and proactive checkpoints.

[English](#en) · [Русский](#ru)

<a id="ru"></a>

## Русский

Набор Markdown-инструкций для сохранения контекста между сессиями AI-агентов. Идея появилась из желания переключаться между агентами и открывать новые чаты без повторного объяснения проекта. Контекст хранится в рабочей папке, а не в конкретном клиенте. Без скриптов, баз данных и зависимости от Git.

[Установка](#ru-setup) · [Использование](#ru-usage) · [Файлы проекта](#ru-files) · [Ограничения](#ru-limits)

[Codex](#ru-codex) · [Claude Code](#ru-claude) · [Google Antigravity](#ru-antigravity) · [Gemini CLI](#ru-gemini) · [Cursor](#ru-cursor) · [OpenCode](#ru-opencode) · [GitHub Copilot CLI](#ru-copilot) · [GitHub Copilot in VS Code](#ru-vscode)

<a id="ru-setup"></a>

### Установка

Скачайте [AGENTS.md](AGENTS.md) и [handoff/SKILL.md](handoff/SKILL.md). Первый содержит постоянные правила, второй — процедуру сохранения и восстановления. Добавьте **содержимое** AGENTS.md в файл инструкций своего клиента (не заменяйте существующие правила), а SKILL.md скопируйте в указанный каталог скилла. Создайте отсутствующие каталоги. Выберите глобальную или проектную установку, не дублируйте скилл. Откройте новую сессию в корне проекта.

В Windows `%USERPROFILE%` можно использовать в проводнике или Win+R, а в PowerShell — `$HOME`. При работе через WSL или удалённую машину используйте домашнюю папку той среды, где запущен агент. Ниже приведены стандартные пути из документации, а не результаты тестирования всех клиентов.

<a id="ru-codex"></a>

#### Codex

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | `~/.codex/AGENTS.md` | `~/.agents/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.codex\AGENTS.md` | `%USERPROFILE%\.agents\skills\handoff\SKILL.md` |
| Проект (все ОС) | `AGENTS.md` | `.agents/skills/handoff/SKILL.md` |

Пример явного сохранения: `$handoff save`

[Документация инструкций](https://learn.chatgpt.com/docs/agent-configuration/agents-md) · [Документация скиллов](https://learn.chatgpt.com/docs/customization/overview)

[К установке](#ru-setup)

<a id="ru-claude"></a>

#### Claude Code

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | `~/.claude/CLAUDE.md` | `~/.claude/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.claude\CLAUDE.md` | `%USERPROFILE%\.claude\skills\handoff\SKILL.md` |
| Проект (все ОС) | `CLAUDE.md` | `.claude/skills/handoff/SKILL.md` |

Claude Code использует CLAUDE.md; одного копирования AGENTS.md под исходным именем недостаточно.

Пример явного сохранения: `/handoff save`

[Документация инструкций](https://code.claude.com/docs/en/memory) · [Документация скиллов](https://code.claude.com/docs/en/skills)

[К установке](#ru-setup)

<a id="ru-antigravity"></a>

#### Google Antigravity

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | `~/.gemini/AGENTS.md` | `~/.gemini/config/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.gemini\AGENTS.md` | `%USERPROFILE%\.gemini\config\skills\handoff\SKILL.md` |
| Проект (все ОС) | `AGENTS.md` | `.agents/skills/handoff/SKILL.md` |

Указаны актуальные пути App/CLI. В старых версиях IDE каталоги могут отличаться; проверьте обнаружение настроек в своей сборке.

Пример явного сохранения: `/handoff save`

[Документация инструкций](https://antigravity.google/docs/rules/) · [Документация скиллов](https://antigravity.google/docs/skills)

[К установке](#ru-setup)

<a id="ru-gemini"></a>

#### Gemini CLI

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | `~/.gemini/GEMINI.md` | `~/.gemini/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.gemini\GEMINI.md` | `%USERPROFILE%\.gemini\skills\handoff\SKILL.md` |
| Проект (все ОС) | `GEMINI.md` | `.gemini/skills/handoff/SKILL.md` |

Пример явного сохранения: `Use the handoff skill in SAVE mode.`

[Документация инструкций](https://geminicli.com/docs/cli/gemini-md/) · [Документация скиллов](https://geminicli.com/docs/cli/skills/)

[К установке](#ru-setup)

<a id="ru-cursor"></a>

#### Cursor

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | User Rules в настройках | `~/.agents/skills/handoff/SKILL.md` |
| Windows | User Rules в настройках | `%USERPROFILE%\.agents\skills\handoff\SKILL.md` |
| Проект (все ОС) | `AGENTS.md` | `.agents/skills/handoff/SKILL.md` |

Пример явного сохранения: `Use the handoff skill in SAVE mode.`

[Документация инструкций](https://cursor.com/docs/rules) · [Документация скиллов](https://cursor.com/docs/skills)

[К установке](#ru-setup)

<a id="ru-opencode"></a>

#### OpenCode

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | `~/.config/opencode/AGENTS.md` | `~/.config/opencode/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.config\opencode\AGENTS.md` | `%USERPROFILE%\.config\opencode\skills\handoff\SKILL.md` |
| Проект (все ОС) | `AGENTS.md` | `.opencode/skills/handoff/SKILL.md` |

Глобальный путь зависит от каталога конфигурации клиента; учитывайте XDG и пользовательские настройки.

Пример явного сохранения: `Use the handoff skill in SAVE mode.`

[Документация инструкций](https://opencode.ai/docs/instructions/) · [Документация скиллов](https://opencode.ai/docs/skills/)

[К установке](#ru-setup)

<a id="ru-copilot"></a>

#### GitHub Copilot CLI

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | `~/.copilot/copilot-instructions.md` | `~/.copilot/skills/handoff/SKILL.md` |
| Windows | `%USERPROFILE%\.copilot\copilot-instructions.md` | `%USERPROFILE%\.copilot\skills\handoff\SKILL.md` |
| Проект (все ОС) | `AGENTS.md` | `.github/skills/handoff/SKILL.md` |

Пример явного сохранения: `Use the handoff skill in SAVE mode.`

[Документация инструкций](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-custom-instructions) · [Документация скиллов](https://docs.github.com/en/copilot/reference/customization-cheat-sheet)

[К установке](#ru-setup)

<a id="ru-vscode"></a>

#### GitHub Copilot in VS Code

| Область | Инструкции | Скилл |
|---|---|---|
| Linux / macOS | Пользовательские инструкции в настройках (или проектный вариант) | `~/.copilot/skills/handoff/SKILL.md` |
| Windows | Пользовательские инструкции в настройках (или проектный вариант) | `%USERPROFILE%\.copilot\skills\handoff\SKILL.md` |
| Проект (все ОС) | `AGENTS.md` | `.github/skills/handoff/SKILL.md` |

Пример явного сохранения: `Use the handoff skill in SAVE mode.`

[Документация инструкций](https://code.visualstudio.com/docs/agents/reference/custom-instructions-reference) · [Документация скиллов](https://code.visualstudio.com/docs/agent-customization/agent-skills)

[К установке](#ru-setup)

<a id="ru-usage"></a>

### Использование

Работайте как обычно, затем отправьте агенту текстовую команду. Это сообщения агенту, а не команды терминала или универсальные slash-команды.

| Команда | Действие |
|---|---|
| `save`, `сохрани` | Сохранить состояние |
| `checkpoint`, `чекпоинт` | Сохранить промежуточный прогресс |
| `resume`, `продолжай` | Восстановить контекст и продолжить разрешённую работу |

Для проверки откройте временный проект, выполните небольшую задачу и напишите `save`. Проверьте HANDOFF.md, откройте новую сессию и напишите `resume`. Сделайте ещё одно изменение и сохраните: предыдущий снимок должен появиться в архиве. Если клиент не загружает скиллы, постоянные правила содержат запасную процедуру. Любой другой агент с доступом к файлам может использовать эти инструкции вручную.

<a id="ru-files"></a>

### Файлы проекта

```text
project/
├── HANDOFF.md
└── .handoff/
    ├── DECISIONS.md
    └── history/
        └── YYYY-MM-DDTHH-MM-SSZ-001.md
```

`HANDOFF.md` — актуальный снимок: цели, фактический прогресс, ограничения, проверки, ошибки, блокеры и следующие шаги. `DECISIONS.md` — значимые решения, доказательства, альтернативы и компромиссы. `history/` — предыдущие снимки; подробные заметки при необходимости хранятся в `.handoff/notes/`. Файлы создаются по мере необходимости. При запуске агент сверяет снимок с реальным состоянием проекта. После значимых этапов предусмотрены промежуточные сохранения. Поддерживаются исследования, инфраструктура, документы и другие задачи без кода.

<a id="ru-limits"></a>

### Ограничения

Это инструкции для агента, а не фоновый сервис. Сохранение при исчерпании лимита, сбое или запрете записи не гарантируется. Синхронизации между устройствами, блокировок параллельной записи и автоматических commit/push нет. Используйте одного записывающего агента за раз. Перед публикацией проверяйте снимки на наличие приватной информации. Не храните учётные данные. Практические тесты совместимости со всеми клиентами не проводились. Пути сверены с указанной документацией 25 ноября 2026 года.

### Благодарности

В основе идеи — [thieung/agent-skills](https://github.com/thieung/agent-skills/tree/main/skills/handoff). В этой версии добавлены история решений, архив снимков и промежуточные сохранения.

[English](#en) · [Русский](#ru)
