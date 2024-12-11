<h1 align="center">SteamTradingSite ID Mapper</h1>

This repository provides an ID mapping for DOTA2 & CS2 tradeable items between the Steam Market and major trading platforms. 

该仓库旨在提供 DOTA2 & CS2 在 Steam Market 与主要的第三方交易平台的饰品 ID 对照表，以便于相关程序的开发。

Currently, we support the following platforms:

- [BUFF](https://buff.163.com/)
- [IGXE](https://www.igxe.cn/)
- [C5](https://www.c5game.com/)
- [UUYP](https://www.youpin898.com/) (youpin898.com)

Please note that we cannot guarantee the completeness, accuracy, or timeliness of the mapping as new items are continuously added to the games. Contributions are always welcome!

请注意，由于游戏中将不断添加新的饰品，我们无法保证对照关系的完整性、正确性与时效性。欢迎发起 PR 进行更新！

## Coverage Rate

|  | **570 (DOTA2)** | **730 (CSGO)** |
| :------: | :-------------: |:--------------:|
| **Steam Market** | 43627 |     23633      |
| **BUFF** | 43337 (99.34%) | 23045 (99.98%) |
| **IGXE** | 28730 (65.85%) | 23347 (98.79%) |
| **C5** | 38668 (88.63%) | 23353 (98.81%) |
| **UUYP** | N/A | 23464 (99.28%) |

## Usage

### Steam

- **Key:** `market_hash_name` of the item.
- **Values:**
  - `en_name`: the display name of the item in English. Please note that this may not always be the same as `market_hash_name`. For more information, please refer to [this discussion](https://www.reddit.com/r/SteamBot/comments/457zpl/question_difference_between_market_name_and/).
  - `cn_name`: the display name of the item in Chinese.
  - `name_id`: the `item_nameid` of the item, which is used in APIs such as [itemordershistogram](https://steamcommunity.com/market/itemordershistogram?country=US&language=english&currency=1&item_nameid=176096390&norender=1).

### Third-party Platforms

- **Key:** `market_hash_name` of the item.
- **Value:** the ID of the item on the respective platform. If the item is currently not found, the value is `-1`.
