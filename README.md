# RaindanceMC/hungergames

- **`hungergames-module`** — Rain's Flexible Modules — Hunger Games: A Hunger Games tournament: the tributes, the teams, the shrinking border, the phases a round goes through, and the screens a gamemaster runs it from. Ported from the plugin of the same name, which carried its own menu framework, its own settings system, its own wording, its own loot and its own sounds — every one of which is RainsCore's here. What is left is the game.
- **`hungergames-standalone`** — Rain's Hunger Games: The Hunger Games, as a plugin of its own. Nothing here but a build file and a descriptor: the hunger games module and the standard wrapper are shaded together, and that is the whole plugin. For a server that already has its own moderation. The jar most people want is hungergames-bundle, which carries both — see its description for why a tournament night in particular needs them together.
- **`hungergames-bundle`** — The Hunger Games: The tournament plugin as it is actually deployed: the hunger games and moderation in one jar, with RainsCore installed alongside. Moderation is not padding here. A tournament is a server full of people who have never met, playing a game whose whole point is being allowed to attack each other — which is exactly the night somebody needs muting, somebody needs looking at, and somebody needs removing. And the two modules are already wired together: a staff rank granted through /promote carries the gamemaster node, so whoever is on shift can run the round without a second list of names being kept anywhere.

Part of [RaindanceMC](https://github.com/RaindanceMC); built on [RainsCore](https://github.com/RaindanceMC/RainsCore) and the shared parent in [framework](https://github.com/RaindanceMC/framework). Split out of `rains-flexible-modules` on 16.10.2026, history kept.

## Build

```
mvn install
```

Needs Java 25 and read access to `packages.tstieh.de` (server ids `packages-releases` / `packages-snapshots` in `~/.m2/settings.xml`).

## Plugins

- `hungergames-standalone/target/RainsHungerGames-2.10.0.jar` — also published as `de.raindancer.modules:hungergames-standalone:2.10.0`
- `hungergames-bundle/target/TheHungerGames-2.9.0.jar` — also published as `de.raindancer.modules:hungergames-bundle:2.9.0`

## Versions

A module's version is a property in this repository's root `pom.xml`, a plugin's is `plugin.version` in its own pom. CI publishes every version that is not in the registry yet on the next push to master.
