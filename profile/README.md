<div align="center">

<a href="https://www.pomvox.ai"><img src="https://raw.githubusercontent.com/pomvox/.github/main/profile/banner.png" alt="Pom, the Pomvox mascot, on a steno pad: Pomvox eats your ums." width="100%" /></a>

[Website](https://www.pomvox.ai) · [Download](https://github.com/pomvox/pomvox/releases/latest/download/Pomvox.dmg) · [Docs](https://www.pomvox.ai/docs) · [Cleanup Engine](https://www.pomvox.ai/engine) · [Blog](https://www.pomvox.ai/blog)

</div>

```sh
brew install --cask pomvox/pomvox/pomvox
```

<sub>Free and open source · macOS 14+ · Apple Silicon · notarized by Apple</sub>

### What Pom does

| you said | Pom wrote |
|---|---|
| um so i think we should like ship the beta on thursday and uh tell the list on friday | I think we should ship the beta on Thursday, and tell the list on Friday. |

**Stays on your Mac.** There is no network code in the transcription path. It works with the Wi‑Fi off.<br/>
**Works in any app.** Mail, Slack, your editor, the terminal. The words land at your cursor.<br/>
**Never makes things up.** Fillers go, punctuation arrives, and when it isn't sure, you get back exactly what you said.

### Repositories

| Repo | What it is |
|---|---|
| [**pomvox**](https://github.com/pomvox/pomvox) | The macOS app. Hold a hotkey, talk, get clean text. |
| [**pomvox-cleanup-engine**](https://github.com/pomvox/pomvox-cleanup-engine) | Swift SDK that turns raw transcripts into text a person would send, locally, with every edit accounted for. |
| [**pomvox-cleanup-mlx**](https://github.com/pomvox/pomvox-cleanup-mlx) | Versioned Apple Silicon MLX runtime for the Cleanup Engine. |
| [**homebrew-pomvox**](https://github.com/pomvox/homebrew-pomvox) | Homebrew tap for installing Pomvox. |

### Use the engine in your own app

```swift
let cleaner = try await Cleaner.open(
    pack: .directory(packURL),
    runtime: .mlx, policy: .local)

let r = try await cleaner.clean(
    CleanupRequest("um please send the pomvox report tomorrow",
                   vocabulary: ["Pomvox"]))
r.text   // "Please send the Pomvox report tomorrow."
```

### Say hello

Questions or ideas: [hello@pomvox.ai](mailto:hello@pomvox.ai) · Security reports: [security@pomvox.ai](mailto:security@pomvox.ai)

<sub>Dictated to Pom by Abhi & Maanasa. No ums were harmed. Several were eaten.</sub>
