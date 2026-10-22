# Graph Report - ClearVision-v6  (2026-10-22)

## Corpus Check
- 143 files · ~82,059 words
- Verdict: corpus is large enough that graph structure adds value.
- Unclassified: 140 file(s) not represented in the graph (top: .scss 134, (none) 5, .css 1)

## Summary
- 480 nodes · 944 edges · 49 communities (22 shown, 27 thin omitted)
- Extraction: 89% EXTRACTED · 11% INFERRED · 0% AMBIGUOUS · INFERRED: 108 edges (avg confidence: 0.88)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Chat Composer & Bars
- Theme Settings & Backgrounds
- Channel Sidebar
- Build, CI & Deploy
- Discord Selector Placeholders
- BD Addons, Embeds & Attachments
- Search, Settings & Profiles
- SCSS Entry & Core Styles
- DevilBro Plugin Support
- Screenshot UI Overview
- Codeblocks & Highlighting
- Titlebar & BD Sidebar
- Messages, Mentions & CV Tags
- Guild List & Anonymify Mod
- Search & Thread Popouts
- Code & Message Buttons Plugins
- Friends Page
- Pins & Thread Modals
- Context & Message Menus
- Misc Popouts
- Activity Feed
- Settings Content
- Avatars & Status
- MemberCount Plugin
- HideChannels Plugin
- Line Numbers Plugin
- Calls & Video
- Radio Groups
- Header Breadcrumbs
- Header Toolbar
- Media Player
- Reactions
- Add Server Modal
- Server Preview
- Emoji Picker
- GIF Picker
- Base Popout
- Stickers
- Channel Settings
- BD Sidebar Icons
- Checkbox
- Header Top Pill
- Message Requests
- Activity Invites
- Keyboard Shortcuts Modal
- Base Modal
- Server Boost Pages
- Group DM Invite
- @everyone Warning

## God Nodes (most connected - your core abstractions)
1. `Accent colors settings (--main/hover/success/danger/url/channel/muted)` - 101 edges
2. `cv() variable lookup function` - 51 edges
3. `App background settings (--background-*)` - 27 edges
4. `stretch mixin (top/right/bottom/left 0)` - 21 edges
5. `Font & text settings (--main-font, --code-font, --text-*)` - 15 edges
6. `DevilBro (BetterDiscord plugin author)` - 12 edges
7. `ClearVision v6-4.7.9 Discord Screenshot` - 12 edges
8. `hover-shadow mixin` - 11 edges
9. `Status colors settings (--online/idle/dnd/offline/streaming)` - 9 edges
10. `pos() position mixin` - 9 edges

## Surprising Connections (you probably didn't know these)
- `Full-Window Background Wallpaper (night landscape)` --conceptually_related_to--> `App background settings (--background-*)`  [INFERRED]
  screenshots/6-stable.4.7.9.png → src/defaultSettings.scss
- `Blue Accent Color` --conceptually_related_to--> `Accent colors settings (--main/hover/success/danger/url/channel/muted)`  [INFERRED]
  screenshots/6-stable.4.7.9.png → src/defaultSettings.scss
- `Presence Status Indicators (online green, offline grey)` --conceptually_related_to--> `Status colors settings (--online/idle/dnd/offline/streaming)`  [INFERRED]
  screenshots/6-stable.4.7.9.png → src/defaultSettings.scss
- `User-editable :root settings overriding defaults` --semantically_similar_to--> `Default theme settings as :root CSS custom properties`  [INFERRED] [semantically similar]
  ClearVision_v6.theme.css → src/defaultSettings.scss
- `GitHub Pages deploy of ./public (peaceiris/actions-gh-pages)` --semantically_similar_to--> `GitLab Pages deploy job (public/)`  [INFERRED] [semantically similar]
  .github/workflows/build.yml → .gitlab-ci.yml

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Discord main layout columns (guilds, channels, chat, members)** — lib_selectors_selectorplaceholders_guilds, lib_selectors_selectorplaceholders_channels, lib_selectors_selectorplaceholders_chat, lib_selectors_selectorplaceholders_members [INFERRED 0.85]
- **SCSS build & deploy pipeline (main.scss -> sass -> public/main.css -> Pages -> theme.css import)** — main, package_scripts_build, github_workflows_build, gitlab_ci, clearvision_v6_theme [INFERRED 0.95]
- **Theme settings resolution (CSS vars -> $cv map -> cv() -> components)** — src_defaultsettings_root_custom_properties, src_variables_cv_map, src_functions_cv, clearvision_v6_theme_user_settings_override [INFERRED 0.95]
- **Filtered background layers (app/backdrop/popout/modal)** — src_defaultsettings_background, src_defaultsettings_backdrop, src_defaultsettings_user_popout, src_defaultsettings_user_modal, src_mixins_filters [INFERRED 0.85]
- **BetterDiscord third-party plugin compatibility styles** — src_bd_plugins_messagebuttons, src_bd_plugins_pluginnotice, src_bd_plugins_arashiryuu_membercount, src_bd_plugins_capnkitten_hidechannels, src_bd_plugins_devilbro_badgeseverywhere, src_bd_plugins_devilbro_datetext, src_bd_plugins_devilbro_gameactivitytoggle, src_bd_plugins_devilbro_ownertag, src_bd_plugins_devilbro_showhiddenchannels, src_bd_plugins_devilbro_tooltips, src_bd_plugins_finicalmist_copycode, src_bd_plugins_noodlebox_linenumbers [EXTRACTED 1.00]
- **Channel sidebar styling (channels, categories, DMs, panels, indicators)** — src_channels_category, src_channels_channelnotice, src_channels_channels, src_channels_indicators, src_channels_panels, src_channels_privatechannels [INFERRED 0.85]
- **Chat area styling** — src_chat_bars, src_chat_call, src_chat_chat, src_chat_divider, src_chat_stagecall [INFERRED 0.85]
- **ClearVision optional mods** — src_cv_mods_animations_mod_animations, src_cv_mods_anonymify_mod_anonymify, src_cv_mods_oldbadge_mod_old_badge, src_cv_mods_privatechannelsvertical_mod_private_channels_vertical [INFERRED 0.95]
- **General form control components themed with accent color** — src_general_checkbox_checkbox, src_general_switch_toggle_switch, src_general_slider_slider, src_general_radiogroup_radio_group, src_general_input_text_input, src_general_button_button_variants [INFERRED 0.85]
- **Message area UI styling files** — src_messages_message, src_messages_embed, src_messages_attachment, src_messages_reaction, src_messages_spoiler, src_messages_mention, src_messages_codeblock [INFERRED 0.85]
- **Home page (friends/activity/library/requests) styling** — src_home_activity, src_home_friends, src_home_library, src_home_requests [INFERRED 0.85]
- **Popouts using cv-menu-fold-y fold-in animation** — src_popouts_contextmenu_context_menu, src_popouts_messageoptions_message_options_popout, src_popouts_messagespopout_inbox_popout [EXTRACTED 1.00]
- **Search inputs with accent focus glow (0 0 2px 2px main color)** — src_pages_discover_discover_search_box, src_pages_studenthub_hub_search_box, src_popouts_emojipicker_emoji_picker, src_popouts_gifpicker_gif_picker [INFERRED 0.85]
- **Popout styling family (dark translucent popouts)** — src_popouts_popout, src_popouts_otherpopouts, src_popouts_searchpopout, src_popouts_stickers, src_popouts_threadpopout, src_popouts_userpopout [INFERRED 0.85]
- **Settings screens styling** — src_settings_sidebar, src_settings_icons, src_settings_content, src_settings_usersettings, src_settings_serversettings, src_settings_channelsettings, src_settings_appconnections [INFERRED 0.85]
- **Custom background layer via stretch+filters+cv()** — src_popouts_userpopout, src_settings_serversettings, src_mixins_stretch, src_mixins_filters, src_functions_cv [EXTRACTED 1.00]
- **ClearVision customizable visual settings shown in screenshot** — screenshots_6_stable_4_7_9_background_wallpaper, screenshots_6_stable_4_7_9_blue_accent, screenshots_6_stable_4_7_9_status_indicators, src_defaultsettings_background, src_defaultsettings_accent_colors, src_defaultsettings_status_colors [INFERRED 0.75]

## Communities (49 total, 27 thin omitted)

### Community 0 - "Chat Composer & Bars"
Cohesion: 0.05
Nodes (39): New messages / jump to present / has more / error bars, Stage channel UI styling, Chat text area / message input styling, Reply bar and mention toggle styling, Slash command option pills, Communication timeout bar/popup, Chat autocomplete popup styling, Slash command autocomplete list (+31 more)

### Community 1 - "Theme Settings & Backgrounds"
Cohesion: 0.05
Nodes (38): BetterDiscord theme metadata header (@name/@version 6.3.0), User-editable :root settings overriding defaults, Theme Editor (bdeditor.dev live preview), App background image layer with filters and overlay, Dual-ring glowing loading spinner, Modal backdrop pseudo-element background, BetterDiscord Custom CSS editor transparency, BD plugin/theme error modal styling (+30 more)

### Community 2 - "Channel Sidebar"
Cohesion: 0.05
Nodes (35): Translucent app notice bar colors per notice type, Collapsed/muted category states, Channel category name with gradient side lines, Channel notice banners (grayscale overlay), Animated selected-channel accent bar, Keyboard focus ring accent, Unread/mention indicator pills, Account panel with hover-revealed theme name/version (+27 more)

### Community 3 - "Build, CI & Deploy"
Cohesion: 0.05
Nodes (37): GitHub Pages deploy of ./public (peaceiris/actions-gh-pages), Upload expanded test/ CSS build artifact, GitLab Pages deploy job (public/), author, bugs, url, contributors, description (+29 more)

### Community 4 - "Discord Selector Placeholders"
Cohesion: 0.09
Nodes (24): App shell, platform & theme classes (appMount, platformWin/OSX/Linux, themeDark/Light, layers, titlebar), BetterDiscord UI (bdEmoteMenu quick-emote menu #bda-qem, bdSettingsSidebar), Channel sidebar (categories, channels, voice users, channel header, guild banner, private channels/DMs), Chat area & composer (chat, channelTextArea, autocomplete, gifPicker, reply bar, upload modal, welcome message), DiscordSelectors v0.2.7, Server discovery & student hubs (discover*, hub*, searchPage), Embeds, attachments, invites & media player (embed*, attachment*, invite*, player*, activityInvite*), Scheduled events, server boosts & stickers (event*, createEvent*, serverBoost*, perksTable, sticker*) (+16 more)

### Community 5 - "BD Addons, Embeds & Attachments"
Cohesion: 0.09
Nodes (14): BetterDiscord addon list/settings UI theming, BD toasts and switches recolored with accent, Custom file-type attachment icons (clearvision.github.io), Attachment upload progress bar, Rich embed text and link styling, Image error grayscale state, Expired invite X icon via pseudo-elements, Server invite embed styling (+6 more)

### Community 6 - "Search, Settings & Profiles"
Cohesion: 0.10
Nodes (15): User profile popout styling, Gradient line channel name separator, Search result context fade mask, Search results panel styling, Per-service brand colour map ($colours @each), Connected accounts settings styling, SCSS map @each icon injection, Settings sidebar tab icons (icon URL maps) (+7 more)

### Community 7 - "SCSS Entry & Core Styles"
Cohesion: 0.11
Nodes (8): $version theme version variable (6.3.0), BetterDiscord select & switch accent styling, Browse Channels page row styling, Screen share source picker and quality settings styling, Server profile notice and nitro upsell transparency, Voice region selector popout styling, Voice channel listening/playing popout styling, Bot tag styling

### Community 8 - "DevilBro Plugin Support"
Cohesion: 0.23
Nodes (7): DevilBro (BetterDiscord plugin author), BadgesEverywhere badge drop-shadow, CreationDate/JoinedAtDate/LastMessageDate text sizing, GameActivityToggle account panel width fix, OwnerTag plugin tag styling, ShowHiddenChannels faded hidden channels, BDFDB tooltip position fix

### Community 9 - "Screenshot UI Overview"
Cohesion: 0.20
Nodes (12): ClearVision v6-4.7.9 Discord Screenshot, Full-Window Background Wallpaper (night landscape), Blue Accent Color, Channel List States (selected / hover / text / muted, expanded / collapsed categories), Chat Message Formatting (bold, italic, underline, strikethrough, inline code, codeblocks, syntax highlighting), Invite Card and YouTube Embed, Welcome to Guild Onboarding Checklist, Member List with Role Groups and Online/Offline Status (+4 more)

### Community 10 - "Codeblocks & Highlighting"
Cohesion: 0.18
Nodes (7): HLJS code-block language display stylesheet, Codeblock pre/hljs container, Inline code styling, Codeblock language label via @each/@extend generated placeholders, $languages highlight.js language map, Code language selector dropdown, Text/file preview container

### Community 11 - "Titlebar & BD Sidebar"
Cohesion: 0.18
Nodes (7): macOS titlebar CV short label, Windows titlebar ClearVision wordmark & version, BetterDiscord emote picker menu styling, BD settings sidebar header/items with slide-in selection, Unofficial source link/invite warning overlay, cv-channel-select keyframe, $main-color / $hover-color shorthands

### Community 12 - "Messages, Mentions & CV Tags"
Cohesion: 0.18
Nodes (8): $tagged map of CV team/donator user IDs, CV user tag badges via avatar src matching, Mention pill styling, Mentioned message highlight, Message jump animation (cv-message-jump), Reply preview styling, Message header/content styling, Thread icons, embeds and jump button

### Community 13 - "Guild List & Anonymify Mod"
Cohesion: 0.29
Nodes (5): ClearVision mod: Anonymify (blurs guild icons and account info for screenshots), Guild folders styling, Guild selection pill indicator, Custom home button background icon, Guild/server list sidebar styling

### Community 14 - "Search & Thread Popouts"
Cohesion: 0.33
Nodes (4): Search datepicker calendar styling, cv-menu-fold-y popout fold animation, Search autocomplete popout styling, Threads popout styling

### Community 15 - "Code & Message Buttons Plugins"
Cohesion: 0.50
Nodes (3): Finicalmist (BetterDiscord plugin author), CopyCode button on code blocks (hover reveal), Quote/reply message buttons (Quoter/Citador plugins) hover reveal

### Community 16 - "Friends Page"
Cohesion: 0.40
Nodes (4): Now Playing / Active Now column, Add Friend tab and input, Friend accept/deny action buttons, Friends list styling

### Community 17 - "Pins & Thread Modals"
Cohesion: 0.40
Nodes (3): Thread modal tabs and thread preview cards, Pinned / recent mentions / unread inbox popout styling, Messages popout tab bar active accent

### Community 18 - "Context & Message Menus"
Cohesion: 0.40
Nodes (3): Context menu with fold-in animation, Danger menu item tinted overlay via pseudo-element, Message options popout with fold-in animation

### Community 19 - "Misc Popouts"
Cohesion: 0.40
Nodes (4): Message hover toolbar styling, Emoji info popout styling, Leave server reason dialog styling, Stream preview popout styling

### Community 20 - "Activity Feed"
Cohesion: 0.50
Nodes (3): Activity feed / home cards styling, Activity feed popout, Quick launcher grid tiles

### Community 21 - "Settings Content"
Cohesion: 0.50
Nodes (3): Settings content region styling, Settings dropdown and input styling, Unsaved changes warning shake animation

## Knowledge Gaps
- **191 isolated node(s):** `autoprefixer`, `postcss-cli`, `prettier`, `rimraf`, `sass` (+186 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 219 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **27 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Accent colors settings (--main/hover/success/danger/url/channel/muted)` connect `Chat Composer & Bars` to `Theme Settings & Backgrounds`, `Channel Sidebar`, `BD Addons, Embeds & Attachments`, `Search, Settings & Profiles`, `SCSS Entry & Core Styles`, `Screenshot UI Overview`, `Codeblocks & Highlighting`, `Titlebar & BD Sidebar`, `Messages, Mentions & CV Tags`, `Guild List & Anonymify Mod`, `Search & Thread Popouts`, `Code & Message Buttons Plugins`, `Friends Page`, `Pins & Thread Modals`, `Context & Message Menus`, `Misc Popouts`, `Activity Feed`, `Settings Content`, `Calls & Video`, `Radio Groups`, `Header Toolbar`, `Media Player`, `Reactions`, `Add Server Modal`, `Server Preview`, `Emoji Picker`, `GIF Picker`, `Base Popout`, `Stickers`, `Channel Settings`, `Checkbox`, `Header Top Pill`, `Message Requests`, `Keyboard Shortcuts Modal`, `Group DM Invite`?**
  _High betweenness centrality (0.150) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `Accent colors settings (--main/hover/success/danger/url/channel/muted)` (e.g. with `Blue Accent Color` and `BetterDiscord color settings (--bd-blue*)`) actually correct?**
  _`Accent colors settings (--main/hover/success/danger/url/channel/muted)` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `autoprefixer`, `postcss-cli`, `prettier` to the rest of the system?**
  _191 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Chat Composer & Bars` be split into smaller, more focused modules?**
  _Cohesion score 0.051759834368530024 - nodes in this community are weakly interconnected._
- **Why does `ClearVision v6-4.7.9 Discord Screenshot` connect `Screenshot UI Overview` to `SCSS Entry & Core Styles`?**
  _High betweenness centrality (0.038) - this node is a cross-community bridge._
- **Are the 4 inferred relationships involving `App background settings (--background-*)` (e.g. with `Full-Window Background Wallpaper (night landscape)` and `Modal backdrop settings (--backdrop-*)`) actually correct?**
  _`App background settings (--background-*)` has 4 INFERRED edges - model-reasoned connections that need verification._
- **Should `Theme Settings & Backgrounds` be split into smaller, more focused modules?**
  _Cohesion score 0.0531986531986532 - nodes in this community are weakly interconnected._