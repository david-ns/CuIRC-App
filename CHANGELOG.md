# Changelog

## Beta 2 (2026-09)

The workspace release. CuIRC is now one app that fits each screen.

### iPad and Mac
- Sidebar workspace with All Chats, Unread and Mentions destinations and servers grouped underneath.
- Chat details inspector beside the conversation, with channel info and a topic editor.
- Conversations in their own windows, movable between windows.
- Window restoration after a restart or a system termination.
- Server reordering from the sidebar.
- Menu bar commands with keyboard shortcuts on iPad and Mac for joining, direct chats, search, sharing and message formatting.
- Mac: immersive surfaces (gallery, editor) presented as panels.

### iPhone
- Home as a list or as cards, with live nicknames in server rows.
- Unread and Mentions filters in the chat list, with reordering under a filter.

### Everywhere
- In-chat search rebuilt: matches highlighted with glass, transcript dimming, and no pull to the bottom while messages arrive.
- A trackpad swipe over the composer reveals search.
- First-launch tour and an About screen.
- Chat wallpaper preview on every device.
- Server colour strip in the server form.
- Redesigned, frost-unified App Lock screen on iPhone and iPad.
- Send preview fills the sheet with matching margins.
- Native bar subtitles, pop-up indicators on selectors, one icon per image provider.
- Clear and Delete in chat options.

### Formatting and sending
- Per-selection styles: bold, italics, underline, strikethrough, mono, text and background colours.
- Several styles in one message.
- Format panel, edit menu and hardware keyboard shortcuts.
- Extended colour palette and reverse video.
- Formatting kept intact across outgoing message splits.
- Undoable composer edits (paste, formatting, completions).
- Copy a message as plain text, rich text or as itself.
- Formatted paste into the composer. Drag formatted selections out of the transcript and composer.
- Send options with app-wide sending policies (split or multiline, line length) and a live preview.
- Outgoing messages split to fit the server's line budget.
- Outbound admission: every command and message is checked against the server's limits before it leaves. Trim, edit or send anyway.
- Command body splitting for `/msg`, `/notice`, `/me` and the console, with confirmation for long commands.
- `/notice` takes a message the way every other command does.
- Quick replies follow the sending policies.

### Channels and people
- Channel topic with setter and date, creation time and website. Set or clear the topic.
- Channel info and modes cached past part, kick and disconnect.
- Ignore people by address, not only by nickname.
- WHO/WHOX identity enrichment for joined channels and stored direct messages, with a persistent identity cache.
- Shared user and channel menus, and a user info sheet that arrives whole.
- Channel user count in the title.
- Service and bouncer conversations (for example ZNC `*status`).
- Conversation history survives a change of spelling.

### IRCv3
- New capabilities: `batch`, `extended-join`, `extended-monitor`, `labeled-response`, `monitor`, `no-implicit-names`, `standard-replies`.
- New tags: `batch`, `bot`, `label`, `msgid`.
- Batch types: `chathistory`, `labeled-response`.
- Bot identity badges.
- Command responses routed to the chat that issued them.
- Server capabilities viewer covers CAP and ISUPPORT.

### Server rules
- Name folding by the server's `CASEMAPPING`, with a persistence migration.
- Channel commands, joins and message targets read under the server's `CHANTYPES`, `STATUSMSG` and `PREFIX`.
- Unadvertised channel prefixes confirmed before joining. Custom channel types supported.
- Advertised length limits honoured: `NICKLEN`, `CHANNELLEN`, `KEYLEN`, `TOPICLEN`, `KICKLEN`, `AWAYLEN`, `USERLEN`, `HOSTLEN`, `NAMELEN`, `LINELEN`.
- Standard replies and join denials answer only their own request.

### Notifications
- Banners show what the message says.
- Mentions decided by what the row recorded.
- Notification Center stays in step with the app.
- Rows recovered from disk are no longer announced as new.
- Orphaned notification conversations summon a main window.

### Fixes
- A cancelled back gesture no longer orphans the chat it lands on.
- Messages from names no user could register are no longer lost.
- A reversed source prefix no longer crashes the client.
- A bare dotted ban mask is read as a host.
- Channels the server considers legal are no longer discarded.
- The join bootstrap burst stays out of the transcript.
- A WHOIS that will never be answered says so.
- Date pill churn while scrolling calmed.
- Wire parser fuzzed against hostile input and checked against the community conformance vectors.

## Beta 1 (2026-07)

Initial public TestFlight release.
