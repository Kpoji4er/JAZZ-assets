# Правила пакета `jazz_assets`

Локальный overlay. Канон комплекта: `../jazz/AGENTS.md`. Навигация: `../jazz/.agents/docs/index.md`. Спеки: `../jazz/docs/specs/active/`. При противоречии действует центральный контракт.

## Владение и ограничения

- Пакет владеет `EntityData`, `.ent`, `.hgm`, `.mtl`, `.mtlbin`, `.dds` и связанными визуальными ресурсами.
- Не переносить сюда формулы оружия, баланс или боевую логику ради удобства.
- Entity Lua и бинарные ресурсы изменять как одну editor/pipeline-транзакцию; перед сохранением и после него запускать sync-аудит.
- После import оружия с numeric DDS нормализовать имена через `$rename-jazz-weapon-textures` (`Entity_MapType.dds`), затем rebuild `mtlbin` в Mod Editor.
- Перед удалением entity проверить parents, states, spots, компоненты оружия и ссылки во всех четырёх пакетах.
- Не добавлять абсолютные пути к исходным FBX/PSD.
- Проверять оружие в руках, на земле и во всех состояниях компонентов; фиксировать runtime evidence или явно отмечать, что проверка была только статической.
- Торс/шлемы Легиона: entity и текстуры здесь; equipped hook и test UnitData — в `jazz` / `jazz-units`.

## Когда что читать

Не открывать все skills. Только совпавшая строка:

| Задача | Открыть |
| --- | --- |
| Поведение, public ID, generated data, межпакетный контракт | spec в `../jazz/docs/specs/active/` + `$specify-jazz-change` |
| Несколько пакетов / ownership | `../jazz/.agents/skills/work-on-jazz-mod/SKILL.md` |
| Editor-generated / `items.lua` / `metadata.lua` | `$sync-jazz-generated-data` |
| Current-state реализации | `../jazz/docs/technical/` |
| Player-facing эффект / drift technical | `../jazz/.cursor/rules/jazz-docs-sync.mdc` + `$document-jazz-systems` |
| Броня/одежда Легиона, HGM, offline QA | `../jazz/.agents/docs/playbooks/legion-armor-modeling.md` |
| Numeric DDS после import ствола | `$rename-jazz-weapon-textures` |
