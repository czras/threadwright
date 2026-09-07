# Threadwright 🧵

Threadwright is infrastructure and methodology for the evolution of intent and knowledge.

It is implementation-agnostic: Threadwright does not require a particular product-management system, development lifecycle, software architecture, or agent architecture. Tooling is a potential implementation of Threadwright, not Threadwright itself.

## Conceptual foundation

### Homo Sapiens Agenticus

**Homo Sapiens Agenticus** is a precursor thesis about human–agent cognitive partnership. It is conceptually independent of Threadwright. It explores how naturally associative human cognition can be complemented by persistent agentic capabilities such as memory, continuity, structural discipline, and relationship management.

See [`methodology/homo-sapiens-agenticus.md`](methodology/homo-sapiens-agenticus.md).

### Threadwright

Threadwright is the infrastructure concept that can operationalize ideas compatible with the HSA thesis: infrastructure for preserving, connecting, evolving, and operationalizing knowledge and intent.

See [`methodology/threadwright.md`](methodology/threadwright.md).

### Methodology

The Threadwright methodology is the implementation-agnostic way of applying the Threadwright approach. It provides a small set of concepts and a continuous control loop for maintaining knowledge, identifying consequential gaps, choosing useful activity, and reassessing what should happen next.

### Heuristics

Heuristics provide reusable reasoning guidance for applying the methodology. They are guidance, not additional fundamental concepts.

### Scenarios

Scenarios demonstrate and challenge the methodology in concrete situations. They are examples and validation material, not prescribed workflows.

### Tooling

Tooling is a potential technological implementation of Threadwright. The repository deliberately keeps the conceptual and methodological model independent of any particular tooling architecture.

Two tooling directions have emerged as areas worth exploring:

- **Implementation design tooling** — tooling that helps humans and agents apply Threadwright to a concrete implementation context while maintaining artifacts, relationships, reasoning, and activities.
- **Artifact system exploration tooling** — tooling for exploring artifacts, relationships, and evolving state.

These are directions for exploration, not a committed product roadmap.

## Repository structure

```text
.
├── methodology/
│   ├── README.md
│   ├── homo-sapiens-agenticus.md
│   ├── threadwright.md
│   ├── heuristics/
│   ├── scenarios/
│   └── artifacts/
├── conventions/
│   ├── artifact-system.md
│   └── git.md
├── meta/
│   └── brand.md
├── README.md
├── LICENSE-SOFTWARE
└── LICENSE-INTELLECTUAL
```

### `methodology/`

The conceptual and methodological body of Threadwright: HSA, Threadwright, the methodology itself, heuristics, scenarios, and the artifacts produced while developing the methodology.

### `conventions/`

Conventions for developing and maintaining this project. They describe repository and artifact-management practices used by the project itself. They support the implementation and evolution of Threadwright but are **not part of the Threadwright conceptual model**.

The distinction is intentional: conventions are about **how this project is developed**, whereas the methodology is about **how a Threadwright-managed body of work is reasoned about and evolved**.

### `meta/`

Project-level identity and brand material. Brand names, marks, and other reserved identity material are not automatically licensed under either repository content license.

## License

Threadwright distinguishes between **software** and **intellectual material** when licensing repository contents.

- **Software** is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. See [`LICENSE-SOFTWARE`](LICENSE-SOFTWARE).
- **Intellectual and documentary material** is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**. See [`LICENSE-INTELLECTUAL`](LICENSE-INTELLECTUAL).

The license follows the **nature of the material**, not its directory. Conceptual, methodological, documentary, and project-governance material is intellectual material; executable software is software.

Neither license grants rights to Threadwright names, logos, trademarks, or other explicitly reserved brand identity unless those rights are separately stated.

## Status

Threadwright is an evolving body of work. Its concepts, methodology, heuristics, scenarios, conventions, and potential tooling are expected to change as they are applied, challenged, and reassessed.
