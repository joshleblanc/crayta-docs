# Analytics

## Class Functions

| Function Name | Return Type | Description | Tag |
| ------------- | ----------- | ----------- | --- |
| Analytics.SendTelemetry([Entity](entity) entity, string type, table parameters) | None | Send an type of telemetry event to the telemetry server with the given entity and parametersTable for later analysis | None |
| Analytics.SendTelemetry(string type, table parameters) | None | Send an type of telemetry event to the telemetry server with the given parametersTable for later analysis | None |
| Analytics.MatchStarted() | [AnalyticsHandle](analytics_handle) | Send a MatchStarted event for later analysis. It is up to the game to define what a match is, for example a single round of a game might be defined as a match. Returns a handle that can be passed to MatchEnded to define the match start and end | None |
| Analytics.MatchEnded([AnalyticsHandle](analytics_handle) matchHandle) | None | Send a MatchEnded event for later analysis | None |
| Analytics.MatchEnded([AnalyticsHandle](analytics_handle) matchHandle, table userEntries) | None | Send a MatchEnded event for later analysis. Takes a table with an entry per user with a 'user' and 'rank' value | None |
| Analytics.Attacked([Entity](entity) attacked, [Entity](entity) victim) | None | Send an Attacked event for later analysis. When an attack entity attack another victim entity. Should be recorded when an attack makes contact or impacts a player or entity | None |
| Analytics.Attacked([Entity](entity) attacker, [Entity](entity) victim, [Entity](entity) weapon) | None | Send an Attacked event for later analysis. When an attack entity attack another victim entity. Should be recorded when an attack makes contact or impacts a player or entity | None |
| Analytics.Defeated([Entity](entity) attacker, [Entity](entity) victim) | None | Send a Defeated event for later analysis. When a player or entity is defeated | None |
| Analytics.PlayerHealthCritical([Entity](entity) playerOrUser) | None | Send a PlayerHealthCritical event for later analysis. When a players health is critically low | None |

## Examples