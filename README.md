# Godzilla Gecko (Minecraft Java, Forge 1.20.1)

Spawn egg is in the Spawn Eggs creative tab, or:
`/summon godzillagecko:godzilla_gecko ~ ~ ~`

## Play it with the Modrinth App
You need the built .jar first (see below), then:
1. Open the Modrinth App > Create instance > Loader: Forge > Game version: 1.20.1.
2. Open the instance > Content > Add content > Add from file > pick `godzillagecko-1.0.0.jar`.
3. Hit Play. Create a world, grab the egg from the Spawn Eggs tab.

## Get the .jar (no setup, free)
1. Make a free GitHub repo and upload everything in this folder (keep the .github folder).
2. Open the repo's Actions tab > "Build mod jar" > Run workflow (it also runs on every push).
3. When it goes green, open the run and download the `godzilla-gecko-jar` artifact. Unzip it.

## Get the .jar (locally)
Install JDK 17 + Gradle 8.1.1 (or copy this folder's files into a Forge 1.20.1 MDK), then:
`gradle build`  ->  jar appears in `build/libs/`.
Live test: `gradle runClient`.

## What it does
- 100 blocks tall, 3000 HP boss bar, fireproof.
- Smashes every block in its body, some blocks fly off as debris.
- Fire breath with predictive aim, explosions + fire where it lands.
- Stomp, tail sweep, trample. Smart attack choice by range/angle/height.
- Below 50% HP it enrages: red skin, faster, longer fire.

## Notes
- Respects the `mobGriefing` gamerule. Don't use Peaceful. Overworld recommended.
- Tune speed/health/size in `GodzillaGeckoEntity.java`; model scale in `GodzillaGeckoRenderer.java`.
