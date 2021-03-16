# Don't touch pls
ConfigVersion: 13.3

# Bot token; don't know what this is? Look at the video on the plugin page for instructions
BotToken: "REDACTED"

# Channel links from game to Discord
# ODIxNDQ0MjcxMTMwNjczMTYx.YFDzlw.yGYJwLcfo_JL9taOo1NvkQUqeiY
# The first channel pair specified in this config option will be the "main" channel, used for sending player joins/quits/deaths/achievements/etc
#
Channels: {"global": "REDACTED"}

# Console channel numerical ID (NOT NAME), leave blank to disable the console channel all together
{"global": "821446292671954974"}

# Debug options, don't touch unless needed
#
# DebugLevel: 0 = no debug, 1 = debug, 2 = debug with stack traces
#
DebugLevel: 0
CancelConsoleCommandIfLoggingFailed: true
DontSendCanceledChatEvents: true

# Disabled plugin hooks
# Generally, unless you have a reason to touch this, don't
#
DisabledPluginHooks: []

# Game information, this sets the "Playing ______" indicator for the bot, set to "" to disable
DiscordGameStatus: "Minecraft Middle Earth"

# Chat channel information
# The chat channel is the text channel that all messages in-game will be sent to and all messages sent
# to this channel on Discord will be sent in-game
#
# DiscordChatChannelDiscordToMinecraft: whether or not to send messages in the chat channel to the server chat
# DiscordChatChannelMinecraftToDiscord: whether or not to send messages in the server chat to the chat channel
# DiscordChatChannelTruncateLength: the maximum length of messages from Discord to be sent to Minecraft
# DiscordChatChannelPrefix: the character(s) required to prefix a message for it to be sent from Minecraft to Discord (example "!")
# DiscordChatChannelRolesAllowedToUseColorCodesInChat: list of roles allowed to use color/format codes in Discord to Minecraft chat
# DiscordChatChannelBroadcastDiscordMessagesToConsole: whether or not to print processed discord messages to the console
# DiscordChatChannelColorTranslations: hex representations of Discord roles to be matched with for showing role colors in-game with their in-game equivalent
#
DiscordChatChannelDiscordToMinecraft: true
DiscordChatChannelMinecraftToDiscord: true
DiscordChatChannelTruncateLength: 200
DiscordChatChannelPrefix: ""
DiscordChatChannelRolesAllowedToUseColorCodesInChat: ["Admin", "Owner", "Admin", "Moderator"]
DiscordChatChannelBroadcastDiscordMessagesToConsole: true
DiscordChatChannelColorTranslations: {
  "99AAB5": "&f",
  "1ABC9C": "&a",
  "2ECC71": "&a",
  "55FFFF": "&b",
  "3498DB": "&3",
  "9B59B6": "&5",
  "E91E63": "&d",
  "F1C40F": "&e",
  "E67E22": "&6",
  "E74C3C": "&c",
  "95A5A6": "&7",
  "607D8B": "&8",
  "11806A": "&2",
  "1F8B4C": "&2",
  "206694": "&1",
  "71368A": "&5",
  "AD1457": "&d",
  "C27C0E": "&6",
  "A84300": "&6",
  "992D22": "&4",
  "979C9F": "&7",
  "546E7A": "&8"
}

# Console channel information
# The console channel is the text channel that receives messages which are then run as server commands
# by the console as well as having the server's console being streamed to line by line
#
# DiscordConsoleChannelLogRefreshRateInSeconds: rate in seconds between sending lines from the console
# DiscordConsoleChannelUsageLog: the file that logs all commands being executed by users in the console channel
# DiscordConsoleChannelBlacklistActsAsWhitelist: whether or not the blacklisted commands list acts as a whitelist instead of blacklist
# DiscordConsoleChannelBlacklistedCommands: phrases wrapped in quotation marks that users should not be able to send as commands to the console
# DiscordConsoleChannelDoNotSendPhrasesActsAsWhitelist: whether or not the do not send phrases list acts as a whitelist instead of blacklist
# DiscordConsoleChannelDoNotSendPhrases: phrases wrapped in quotation marks that should not be sent to the console channel
# DiscordConsoleChannelRegexFilter: the regex filter to be applied to console lines being sent to Discord ("\[\d+:\d+:\d+ \w+\]: " will remove time stamps)
# DiscordConsoleChannelRegexReplacement: what the regex filter will replace with where matches are found
# DiscordConsoleChannelLevels: levels to send to console channel via appender
#
DiscordConsoleChannelLogRefreshRateInSeconds: 5
DiscordConsoleChannelUsageLog: "DiscordConsole.log"
DiscordConsoleChannelBlacklistActsAsWhitelist: false
DiscordConsoleChannelBlacklistedCommands: ["?", "op", "deop"]
DiscordConsoleChannelDoNotSendPhrasesActsAsWhitelist: false
DiscordConsoleChannelDoNotSendPhrases: ["Async Chat Thread"]
DiscordConsoleChannelRegexFilter: ""
DiscordConsoleChannelRegexReplacement: ""
DiscordConsoleChannelLevels: ["info", "warn", "error"]

# Chat channel command execute command
# These options control the ability to say "!c kick Notch", or whatever the prefix is to run a command,
# as the console, from a registered chat channel.
#
# DiscordChatChannelConsoleCommandEnabled: whether or not to allow console commands from a chat channel.
# DiscordChatChannelConsoleCommandNotifyErrors: whether or not to send a user who tries to run a command without permission that they don't have permission
# DiscordChatChannelConsoleCommandPrefix: prefix to use for console commands. e.g. "!c tps"
# DiscordChatChannelConsoleCommandRolesAllowed: the user roles that are allowed to execute server commands from the chat channel
# DiscordChatChannelConsoleCommandWhitelist: list of commands that are able to be ran with DiscordChatChannelConsoleCommandPrefix
# DiscordChatChannelConsoleCommandWhitelistBypassRoles: list of roles that bypass the whitelist
# DiscordChatChannelConsoleCommandWhitelistActsAsBlacklist: should the command whitelist act as a blacklist instead
# DiscordChatChannelConsoleCommandExpiration: time in seconds until a sent command output is automatically removed by the bot. set to 0 to disable expiration.
# DiscordChatChannelConsoleCommandExpirationDeleteRequest: whether or not to delete the message of the person that originally issued the command
#
DiscordChatChannelConsoleCommandEnabled: true
DiscordChatChannelConsoleCommandNotifyErrors: true
DiscordChatChannelConsoleCommandPrefix: "!c"
DiscordChatChannelConsoleCommandRolesAllowed: ["Admin", "Owner"]
DiscordChatChannelConsoleCommandWhitelist: ["say", "lag", "tps"]
DiscordChatChannelConsoleCommandWhitelistBypassRoles: ["Admin", "Developer"]
DiscordChatChannelConsoleCommandWhitelistActsAsBlacklist: false
DiscordChatChannelConsoleCommandExpiration: 0
DiscordChatChannelConsoleCommandExpirationDeleteRequest: true

# Chat channel player list command
# All the config stuff for the player list command
#
# DiscordChatChannelListCommandEnabled: whether the command is enabled
# DiscordChatChannelListCommandMessage: the command people can type to get the player list
# DiscordChatChannelListCommandExpiration: time in seconds until a sent player list message is automatically removed by the bot. set to 0 to disable expiration.
# DiscordChatChannelListCommandExpirationDeleteRequest: whether or not to delete the message of the person that originally requested for the player list
#
DiscordChatChannelListCommandEnabled: true
DiscordChatChannelListCommandMessage: "playerlist"
DiscordChatChannelListCommandExpiration: 10
DiscordChatChannelListCommandExpirationDeleteRequest: true

# Chat channel blacklisted phrases & regex
#
# DiscordChatChannelBlockedPhrases: phrases which if a message is sent in the chat channel containing a phrase here, the message won't be processed
# DiscordChatChannelCutPhrases: phrases which if said in the Minecraft chat will be removed from the message before sending it to the chat channel
# DiscordChatChannelRegex: regex to filter the chat going to Minecraft by
# DiscordChatChannelRegexReplacement: replacement for above option
#
DiscordChatChannelBlockedPhrases: ["Online players (", "**No online players**"]
DiscordChatChannelCutPhrases: ["@everyone"]
DiscordChatChannelRegex: ""
DiscordChatChannelRegexReplacement: ""

# Channel topic updater settings
#
# ChannelTopicUpdaterChannelTopicsAtShutdownEnabled: whether or not the channel topics should be changed at server shutdown at all
# ChannelTopicUpdaterRateInSeconds: amount of seconds between automatically updating the channel topics with fresh information
#
ChannelTopicUpdaterChannelTopicsAtShutdownEnabled: true
ChannelTopicUpdaterRateInSeconds: 5

# Unsubscribed user message forwarding
# Whether or not people who are unsubscribed from Discord chat messages will still have their messages
# sent to the chat channel, yet still not see anything from the chat channel
#
MinecraftUnsubscribedMessageForwarding: false

# Discord canned responses
# These are triggers (commands in a way) that will trigger a "canned response" to be sent as a reply to them
# You should probably change these from their defaults or add your own
#
# Syntax is {"TRIGGER": "RESPONSE", "TRIGGER": "RESPONSE", ...}
# If you do not want any canned responses, set this to just {}
# PlaceholderAPI placeholders are supported
#
DiscordCannedResponses: {"!ip": "yourserveripchange.me", "!site": "http://yoursiteurl.net"}

# Minecraft to Discord account linking
# These are the config options pertaining to how linking a Minecraft account to a Discord account functions
#
# MinecraftDiscordAccountLinkedConsoleCommands: commands to run when an account is linked, see below for possible placeholders
# %minecraftplayername%: player's Minecraft username
#                         example: Notch
# %minecraftuuid%:       player's uuid
#                         example: you know what a uuid looks like
# %discordid%:           linked discord account's id
#                         example: 12345678901234567890
# %discordname%:         linked discord account's username
#                         example: Notch
#
# MinecraftDiscordAccountLinkedRoleToAddUserTo: the name of a discord role to add a discord user to when they link their account
# MinecraftDiscordAccountLinkedSetDiscordNicknameAsInGameName: whether or not to set the discord user's nickname to their in-game account name
#
MinecraftDiscordAccountLinkedConsoleCommands: ["", "", ""]
MinecraftDiscordAccountLinkedRoleNameToAddUserTo: "Linked"
MinecraftDiscordAccountLinkedSetDiscordNicknameAsInGameName: false

# Minecraft -> Discord role synchronization
#
# Syntax is {"in-game group name": "discord role name", "in-game group name": "discord role name", ...)
# If you do not want role synchronization, set this to just {}
#
GroupRoleSynchronizationRolesToSynchronize: {"root": "Admin", "enforcervalar": "Head Enforcer", "buildvalar": "Head Designer", "enforcer": "Enforcer", "designer": "Designer", "foreman": "Foreman", "artist": "Artist", "guide": "Guide", "commoner": "Commoner"}

# Server watchdog
#
# The watchdog constantly monitors the last time your server performed a game tick
# If the time since the last tick goes above the set interval in seconds, Discord messages can be triggered
#
# ServerWatchdogEnabled: whether or not the watchdog is enabled at all
# ServerWatchdogTimeout: time in seconds that need to elapse before the watchdog takes action (Spigot's crash detection uses 60 for this)
#                        the minimum for this value is 10
# ServerWatchdogMessageCount: the amount of times ServerWatchdogMessage is sent. useful if you *really* want to make sure you know something's up
#
ServerWatchdogEnabled: true
ServerWatchdogTimeout: 30
ServerWatchdogMessageCount: 3

# Ban synchronization
# When a player gets banned on the server when they have a linked Discord account you can optionally ban them on the Discord server and vice versa
#
# BanSynchronizationDiscordToMinecraft: whether or not to ban people on the Minecraft server if they get banned from the Discord server
# BanSynchronizationDiscordToMinecraftReason: the message to be used as the ban reason for banning players from the Minecraft server
# BanSynchronizationMinecraftToDiscord: whether or not to ban people on the Discord server if they get banned from the Minecraft server
#
BanSynchronizationDiscordToMinecraft: true
BanSynchronizationDiscordToMinecraftReason: "&cYou have been banned until further notice from the server because you were banned on our Discord server."
BanSynchronizationMinecraftToDiscord: true
