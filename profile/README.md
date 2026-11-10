<p align="center">
  <a href="https://jakta-bdi.github.io/"><img src="https://jakta-bdi.github.io/img/logo.svg" alt="JaKtA logo" width="120"></a>
</p>

<h1 align="center">JaKtA</h1>

<p align="center">
  <b>BDI agents as a Kotlin Multiplatform DSL</b><br>
  <a href="https://jakta-bdi.github.io/">Website</a> ·
  <a href="https://jakta-bdi.github.io/docs/intro">Docs</a> ·
  <a href="https://github.com/orgs/jakta-bdi/discussions">Discussions</a> ·
  <a href="https://jakta-bdi.github.io/api/">API</a> ·
  <a href="https://central.sonatype.com/namespace/it.unibo.jakta">Maven Central</a> ·
  <a href="https://doi.org/10.1007/s42979-024-03244-y">Paper</a>
</p>

JaKtA is a Belief-Desire-Intention (BDI) agent-oriented programming framework.
Agents, their beliefs, goals and plans are written side by side with ordinary Kotlin code,
and run on the JVM, in JavaScript (browser and Node.js) and natively.

```kotlin
val hello = agent<String, String, Any> {
    embodiedAs { Any() }
    hasInitialGoals { !"sayHello" }
    hasPlanLibrary {
        adding.goal { takeIf { it == "sayHello" } } triggers {
            agent.print("Hello, world!")
            node.terminateNode()
        }
    }
}
```

Start from the [**website**](https://jakta-bdi.github.io/): tutorials, how-to guides, concepts and showcase applications.

## Repositories

| Repository | What it is |
|---|---|
| [jakta](https://github.com/jakta-bdi/jakta) | The framework: core engine, DSL, Prolog and string incarnations, Alchemist integration, examples and website sources |
| [jakta-bdi.github.io](https://github.com/jakta-bdi/jakta-bdi.github.io) | Deployed website and API reference |

## Get involved

- 💬 Questions, ideas or something you built with JaKtA? Join the [**Community discussions**](https://github.com/orgs/jakta-bdi/discussions).
- 🐛 Found a bug? Open an [issue](https://github.com/jakta-bdi/jakta/issues).

JaKtA is developed by the [Pervasive Software Lab](https://pslab-unibo.github.io/) at the University of Bologna
and released under the Apache 2.0 license.

If you use JaKtA in research, please cite
[*Blending BDI Agents with Object-Oriented and Functional Programming with JaKtA*](https://doi.org/10.1007/s42979-024-03244-y)
(SN Computer Science, 2024).
