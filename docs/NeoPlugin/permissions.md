---
sidebar_position: 3
title: Permissions
---

# Permissions

You have to set the permission ``neoprotect.admin`` before you can start the setup.

| Command / Feature    | Description                                                 | Permission                             |
|:---------------------|-------------------------------------------------------------|----------------------------------------|
| /np setup            | start the setup (setup set API-KEY, backend and gameshield) | neoprotect.admin                       |
| /np ipanic           | toggle AntiBot level                                        | neoprotect.admin                       |
| /np toggle (option)  | toggle different options                                    | neoprotect.admin                       |
| /np debugTool        | start debug tool                                            | neoprotect.admin                       |
| /np setgameshield    | set gameshield for establish the connection to NeoProtect   | neoprotect.admin                       |
| /np setbackend       | set backend for establish the connection to NeoProtect      | neoprotect.admin                       |
| under attack message | In-game message if server is under attack                   | neoprotect.admin<br/>neoprotect.notify |
