# Custom variation of TTT Role pack

## Randoman
_Contributed By_: The Stig\
The Randoman is a detective who is able to buy randomat events, rather than detective items.\
_Requires [TTT Randomat 2.0 for Custom Roles for TTT](https://steamcommunity.com/sharedfiles/filedetails/?id=2055805086) to be installed._
\
\
**ConVars**
```cpp
ttt_randoman_enabled                    0      // Whether or not the randoman should spawn
ttt_randoman_spawn_weight               1      // The weight assigned to spawning the randoman
ttt_randoman_min_players                0      // The minimum number of players required to spawn the randoman
ttt_randoman_starting_health            100    // The amount of health a randoman starts with
ttt_randoman_max_health                 100    // The maximum amount of health a randoman can have
ttt_randoman_banned_randomats           "lame" // Events not allowed in the randoman's shop, separate ids with commas. You can find an ID by turning a randomat on/off in the randomat ULX menu and copying the word after 'ttt_randomat_', which appears in chat.
ttt_randoman_prevent_auto_randomat      1      // Prevent auto-randomat triggering if there is a randoman at the start of the round.
ttt_randoman_guaranteed_categories      "biased_innocent,fun,moderateimpact" // A randomat from these categories is guaranteed be in the randoman's shop, separate categories with commas. Categories: biased_innocent, biased_traitor, biased_zombie, biased, deathtrigger, entityspawn, eventtrigger, fun, gamemode, item, largeimpact, moderateimpact, rolechange, smallimpact, spectator, stats
ttt_randoman_guaranteed_randomats       ""     // These events are guaranteed be in the randoman's shop, separate event IDs with commas.
ttt_randoman_event_on_unbought_death    0      // Whether a randomat should trigger if a randoman dies and never bought anything that round
ttt_randoman_choose_event_on_drop       1      // Whether the held randomat item should always trigger "Choose an event!" after being bought by a randoman and dropped on the ground
ttt_randoman_choose_event_on_drop_count 5      // The number of events a player should be able to choose from when using a dropped randomat
ttt_randoman_guarantee_pockets_event    1      // Whether the "What did I find in my pocket?" event should always be available in the randoman's shop while the beggar role is enabled
ttt_randoman_credits_starting           1      // The number of credits a randoman should start with
ttt_randoman_shop_sync                  0      // Whether a randoman should have all weapons that vanilla detectives have in their weapon shop
ttt_randoman_shop_random_percent        0      // The percent chance that a weapon in the shop will be not be shown for the randoman
ttt_randoman_shop_random_enabled        0      // Whether role shop randomization is enabled for the randoman
ttt_randoman_is_independent             0      // Whether the randoman is an independent role
ttt_randoman_can_see_jesters            1      // Whether jesters are revealed (via head icons, color/icon on the scoreboard, etc.) to the randoman (if ttt_randoman_is_independent is enabled)
ttt_randoman_update_scoreboard          1      // Whether the randoman shows dead players as missing in action (if ttt_randoman_is_independent is enabled)
```

## Santa
_Suggested By_: [The Custom Roles for TTT Discord Server](https://discord.gg/BAPZrykC3F) \
Santa is a detective who is able to give gifts to nice players and coal to naughty players.
\
\
**ConVars**
```cpp
ttt_santa_enabled                  0   // Whether or not the santa should spawn
ttt_santa_spawn_weight             1   // The weight assigned to spawning the santa
ttt_santa_min_players              0   // The minimum number of players required to spawn the santa
ttt_santa_starting_health          100 // The amount of health a santa starts with
ttt_santa_max_health               100 // The maximum amount of health a santa can have
ttt_santa_random_presents          0   // Whether santa should give random presents instead of being able to choose presents from the shop
ttt_santa_jesters_are_naughty      1   // Whether jesters are considered to be "naughty" players
ttt_santa_independents_are_naughty 0   // Whether independents are considered to be "naughty" players
ttt_santa_set_gift_owner           0   // Whether gifts given by santa should be owned by them for the purposes of roles that react to the original weapon buyer (e.g the beggar)
ttt_santa_credits_starting         1   // The number of credits a santa should start with
ttt_santa_shop_sync                0   // Whether a santa should have all weapons that vanilla detectives have in their weapon shop
ttt_santa_shop_random_percent      0   // The percent chance that a weapon in the shop will be not be shown for the santa
ttt_santa_shop_random_enabled      0   // Whether role shop randomization is enabled for the santa
```

**Hooks**
#### TTTSantaPresentOpened(ply, tgt, item_id)
Called when a player opens a present from santa.\
*Realm:* Server\
*Parameters:*
- *ply* - The santa who provided the present
- *tgt* - The player who opened the present
- *item_id* - The ID of the item/equipment in the present
