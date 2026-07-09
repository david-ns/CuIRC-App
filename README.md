<p align="center">
  <img src="resources/logo.png" alt="CuIRC" width="128" height="128">
</p>
<p align="center">
  <h1 align="center">CuIRC</h1>
  <p align="center">
    <em>Cui cui cui!</em> — A native IRC client for iPhone, iPad, and Mac.
  </p>
</p>

<p align="center">
  <a href="https://testflight.apple.com/join/VmrhH4bc"><img src="https://img.shields.io/badge/TestFlight-Join%20the%20beta-0D96F6?logo=apple&logoColor=white" alt="Join the TestFlight beta"></a>
  <img src="https://img.shields.io/badge/beta-1.0%20(4)-blueviolet" alt="Latest TestFlight beta 1.0 build 4">
  <img src="https://img.shields.io/badge/platform-iOS%20%7C%20iPadOS%20%7C%20macOS%2026%2B-lightgrey" alt="Platforms">
  <img src="https://img.shields.io/badge/languages-24-orange" alt="24 languages">
</p>

---

**CuIRC** is a native IRC client for iPhone, iPad, and Mac. The name is a play on how guinea pigs chat (*cui cui cui* 🐹) and, of course, IRC. It's written from scratch in UIKit with Liquid Glass styling and a SwiftNIO networking core, plus the platform touches you'd want on modern iOS: Dynamic Island, Live Activities, rich text, Dynamic Type, and localization in 24 languages.

This repo is where CuIRC lives in public. Report bugs, request features, and see what's coming next. The app is a public TestFlight beta, so anyone can join.

## 📲 Join the beta

CuIRC is in open **TestFlight** beta:

### 👉 [testflight.apple.com/join/VmrhH4bc](https://testflight.apple.com/join/VmrhH4bc)

1. Install [TestFlight](https://apps.apple.com/app/testflight/id899247664) from the App Store.
2. Open the [invite link](https://testflight.apple.com/join/VmrhH4bc) above and tap **Accept**.
3. Tap **Install** and start chatting.

**Requires** iOS 26+, iPadOS 26+, or macOS 26+.

> Beta builds change fast. If something breaks, please tell us — see [Reporting issues](#-reporting-issues--feedback) below.

## ✨ Highlights

**Modern & native**
- Fully native UIKit interface with Liquid Glass styling.
- Full Dynamic Type support.
- Localized in 24 languages.

**Rich, real-time chat**
- Rich text formatting — bold, italic, underline, strikethrough, mono, and colors.
- Inline URL previews, image previews with a gallery, and link/chat peek.
- Mention highlighting, swipe-to-reply, and smart scrolling that remembers where you left off.
- Per-target unread tracking, timestamps, and a floating date indicator.

**Power features**
- **Location-based profiles** — automatically connect or disconnect from servers based on where you are and what time it is.
- **Location sharing** with Live Activity + Dynamic Island, one-time or recurring.
- **Image upload & editor** (Catbox, ImgBB) with crop, rotate, watermark, adjust, censor, and draw tools.

**IRC support**
- IRCv3 capability negotiation, message tags, and `multi-prefix` roles.
- Authentication via SASL, NickServ, and ZNC.
- WHOIS, channel modes, channel discovery, and user lists.
- Moderation tools: kick, ban (with mask helper), and role management.
- Per-user ignore, slash commands with helpers, and multiline handling.

**Notifications**
- Per-scope rules (global, server, chat) for messages, mentions, and system events.
- Reply directly from a notification, with deep links into the conversation.
- Custom rules that let you define your own keyword and pattern triggers to get notified (and highlight matching messages) beyond plain mentions.

## 🔌 IRCv3 capabilities

Where CuIRC stands on the IRCv3 spec today. Supported caps are negotiated automatically on connect (`sasl` only when you've configured authentication).

> **Goal:** we aim to support every capability in the [IRCv3 registry](https://ircv3.net/registry) that isn't marked `[draft]` or `[deprecated]`. The tables below track current progress.

| Capability | Supported |
|---|:---:|
| `account-notify` | ✅ |
| `account-tag` | ✅ |
| `away-notify` | ✅ |
| `cap-notify` | ✅ |
| `chghost` | ✅ |
| `invite-notify` | ✅ |
| `message-tags` | ✅ |
| `multi-prefix` | ✅ |
| `sasl` | ✅ |
| `server-time` | ✅ |
| `setname` | ✅ |
| `userhost-in-names` | ✅ |
| `batch` | 🚧 Planned |
| `echo-message` | 🚧 Planned |
| `extended-join` | 🚧 Planned |
| `extended-monitor` | 🚧 Planned |
| `labeled-response` | 🚧 Planned |
| `monitor` | 🚧 Planned |
| `standard-replies` | 🚧 Planned |

### Message tags

| Tag | Supported | Requires |
|---|:---:|---|
| `account` | ✅ | `account-tag` |
| `time` | ✅ | `server-time` |
| `batch` | 🚧 Planned | `batch` |
| `bot` | 🚧 Planned | `message-tags` |
| `msgid` | 🚧 Planned | `message-tags` |
| `+reply` | 🚧 Planned | `message-tags` |
| `+typing` | 🚧 Planned | `message-tags` |

You can inspect what a server advertised versus what got negotiated from the in-app server capabilities viewer.

## 🗺️ Roadmap

Planned and in-progress work lives in [Issues](../../issues) and [Milestones](../../milestones). A few things on the way:

- Channel mode management UI
- Chat export & message translation
- Universal search
- More IRCv3 capabilities (see the [matrix above](#-ircv3-capabilities))
- **Longer term:** tailor-made iPad/Mac layouts, ZNC push plugin, DCC, iCloud Sync

## 🐛 Reporting issues & feedback

Found a bug or have an idea? This is the place.

- **[Report a bug](../../issues/new/choose)**: include your device, OS version, and steps to reproduce.
- **[Request a feature](../../issues/new/choose)**: tell us what you're trying to do.
- **[Discussions](../../discussions)** for questions, ideas, and general chat.

A quick search of [existing issues](../../issues) first helps avoid duplicates.

## 🔒 Privacy

Your data stays on your device.

- **No account, no tracking.** CuIRC has no backend of its own; it talks directly to the IRC servers you configure.
- **Location** is only used for the features you turn on (location-based profiles, location sharing), and only while they're enabled.
- **Images** upload only when you choose to, to the third-party host you pick (Catbox or ImgBB).
- Servers, credentials, and history are stored locally on your device.

## 🙌 Credits

CuIRC's IRC core uses code from the open-source [swift-nio-irc](https://github.com/SwiftNIOExtras/swift-nio-irc) and [swift-nio-irc-client](https://github.com/NozeIO/swift-nio-irc-client) (Apache 2.0), built on Apple's [SwiftNIO](https://github.com/apple/swift-nio). Full third-party acknowledgements are available in the app's Settings.

## License

CuIRC is proprietary software, free to use during the beta. The source code is not open. Third-party components retain their original licenses (see in-app acknowledgements).

---

<p align="center">
  Made with 🧡 and a lot of <em>cui cui cui</em> and <em>prrrrr</em>.
</p>
