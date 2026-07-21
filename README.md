# AI Engineering Agent System

Hordozható, szerepkör-alapú agent rendszer szoftverfejlesztési feladatokhoz. A rendszer nem egy adott modell vagy SDK futtatókörnyezete: a Markdown fájlok a szerepkörök teljes instrukciói. Add át őket az általad használt agent platformnak, vagy hivatkozz rájuk a projekt saját utasításaiban.

## Szerepkörök

| Agent | Felelősség |
| --- | --- |
| [Orchestrator](agents/orchestrator.md) | Feladatbontás, sorrendezés, átadás, végső összehangolás |
| [Researcher](agents/researcher.md) | Kódbázis- és dokumentációkutatás, bizonyíték-alapú megállapítások |
| [Planner](agents/planner.md) | Megvalósítható, tesztelhető terv készítése |
| [Executor](agents/executor.md) | Jóváhagyott terv biztonságos implementálása |
| [Code reviewer](agents/code-reviewer.md) | Hibák, regressziók és kockázatok felderítése |
| [Verifier](agents/verifier.md) | Cél-visszafejtéses ellenőrzés és kiadási döntés |

## Ajánlott folyamat

1. Az **orchestrator** a felhasználói igényt egy `TASK-BRIEF` formátumú feladattá alakítja.
2. A **researcher** feltárja az érintett kódot és a meglévő mintákat.
3. A **planner** tervet ír; nagyobb vagy kockázatos változtatás csak ezután lép implementációba.
4. Az **executor** elvégzi a változtatásokat és futtatja a releváns ellenőrzéseket.
5. A **code reviewer** és a **verifier** egymástól függetlenül értékeli az eredményt.
6. Az **orchestrator** csak akkor zárja le a munkát, ha a kritikus megállapítások megoldódtak.

A közös átadási sablon: [TASK-BRIEF.md](protocols/TASK-BRIEF.md). A teljes életciklus szabályai: [WORKFLOW.md](protocols/WORKFLOW.md).
