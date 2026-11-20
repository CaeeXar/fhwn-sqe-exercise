# Contributing

## IDs

| ID                               | Item                                           | Defined in                               |
| -------------------------------- | ---------------------------------------------- | ---------------------------------------- |
| `REQ-nn`                         | Requirement                                    | `docs/requirements.md`                   |
| `US-nn`                          | User story                                     | `docs/user-stories.md`                   |
| `AC-nn.m`                        | Acceptance criterion m of US-nn                | `docs/user-stories.md`                   |
| `DES-nn`                         | Design element (module, interface, class)      | `docs/architecture.md`, `docs/design.md` |
| `UT-nn.m`, `IT-nn.m`, `E2E-nn.m` | Unit, integration, end-to-end test m for US-nn | `docs/test-design.md`                    |

- IDs are never reused or renumbered. A dropped item keeps its ID and is marked "removed".
- A test method name starts with its test ID, using underscores: `UT03_2_DepositOfZero_IsRejected`.
- Adding, changing or removing any of these items updates `docs/traceability-matrix.md` in the same pull request.

## Git

- One branch per step: `<type>/<topic>`, type `docs`, `feature`, `test` or `fix`, e.g. `feature/US-03-deposit`.
- Commit message: `<IDs>: <imperative summary>`, e.g. `US-03, AC-03.2: Reject deposits of zero`. Code commits name at least one user story. Commits without an item use `chore:`.
- Pull request title in commit format; the description lists the covered IDs. The other team member reviews before merging.
- Pull requests are squash-merged, so each pull request is one commit on `main` carrying its IDs. The traceability matrix references commits by pull request number (`#12`), entered when the pull request is opened.
