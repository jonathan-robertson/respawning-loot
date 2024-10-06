# Renewable Loot

[![🧪 Tested On 7DTD 1.1 (b14)](https://img.shields.io/badge/🧪%20Tested%20On-7DTD%201.1%20(b14)-blue.svg)](https://7daystodie.com/) [![📦 Automated Release](https://github.com/jonathan-robertson/respawning-loot/actions/workflows/release.yml/badge.svg)](https://github.com/jonathan-robertson/respawning-loot/actions/workflows/release.yml)

- [Renewable Loot](#renewable-loot)
  - [Summary](#summary)
    - [Support](#support)
  - [Features](#features)

## Summary

A simple mod that keeps many containers from breaking when they are looted; similar to how things were before A21.

### Support

🗪 If you would like support for this mod, please feel free to reach out via [Discord](https://discord.gg/tRJHSB9Uk7).

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
