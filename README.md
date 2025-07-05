# Respawning Loot [![Status: 💟 End of Life](https://img.shields.io/badge/💟%20Status-End%20of%20Life-blue.svg)](#support)

[![🧪 Tested On 7DTD 1.1 (b14)](https://img.shields.io/badge/🧪%20Tested%20On-7DTD%201.1%20(b14)-blue.svg)](https://7daystodie.com/) [![📦 Automated Release](https://github.com/jonathan-robertson/respawning-loot/actions/workflows/release.yml/badge.svg)](https://github.com/jonathan-robertson/respawning-loot/actions/workflows/release.yml)

- [Summary](#summary)
  - [Support](#support)
- [Features](#features)

## Summary

A simple mod that keeps many containers from breaking when they are looted; similar to how things were before A21.

> 💟 This mod has reached [End of Life](#support) and will not be directly updated to support 7 Days to Die 2.0 or beyond. Because this mod is [MIT-Licensed](LICENSE) and open-source, it is possible that other modders will keep this concept going in the future.
>
> Searching [NexusMods](https://nexusmods.com) or [7 Days to Die Mods](https://7daystodiemods.com) may lead to discovering other mods either built on top of or inspired by this mod.

### Support

💟 This mod has reached its end of life and is no longer supported or maintained by Kanaverum ([Jonathan Robertson](https://github.com/jonathan-robertson) // me). I am instead focused on my own game studio ([Calculating Chaos](https://calculatingchaos.com), if curious).

❤️ All of my public mods have always been open-source and are [MIT-Licensed](LICENSE); please feel free to take some or all of the code to reuse, modify, redistribute, and even rebrand however you like! The code in this project isn't perfect; as you update, add features, fix bugs, and otherwise improve upon my ideas, please make sure to give yourself credit for the work you do and publish your new version of the mod under your own name :smile: :tada:

## Features

Prevent `auto-destroy` functionality for all loot containers ***except for the following***:

Loot Container Name | Reason for Exclusion
--- | ---
`playerBackpack` | dropped backpacks are entities and should be destroyed once emptied
`airDrop` | air drops are entities and should be destroyed once emptied
`%buried%` / `%Buried%` | any container with the key word `buried` also configured to disappear on loot should be allowed to do so (causes bugs otherwise)
`questRewardSkillMagazines` | these quest rewards are meant to be looted only once
`%infested%` | special containers rewarded to players who complete infested quests should only be looted once
`%twitch%` | any twitch-related or twitch-spawned containers shouldn't remain once looted

> NOTE: Bags dropped by zombies are not managed by the `destroy_on_close`; some other part of the code handles their cleanup and they will continue to function as they always have.
