# mmorpg-vuetify-admin-dashboard
Admin dashboard made with vue.js 2 / vuetify 2 for mmorpg game Lineage 2 Interlude

My first big project was https://la2dream.com Lineage II Interlude MMORPG website with admin dashboard.
For Frontend and Admin dashboard i've used Vue.js 2 and for the Backend REST API i've used CodeIgniter 4 framework.

There is such function as signup, restore password, restore username, change password, change email, unbind character (by HWID [HardWare ID] in game), many payment system's implemented in 2+ years (10+), statistics, top characters / clans / pk / pvp.. Also castle attackers / defenders, search character's from website.. 

Also there was SMTP paid providers which have banned us because of high bounce rate (admin's choice to accept only email verified users), i have spinned up smtp server through docker on my personal VPS server and administrating it - which cost about 6 eur / month, which is great price for 4C / 8G / 200G SSD...

To prevent redundant connection first thing i've done is to try save json encoded data from REST API sever into browser's storage. If user have disabled cookies / storage library - no problem, we are fetching from file cached / redis storage on api server. That's not all, if cache is the same, we don't want to send each time excess KB - that's why we used HTTP Cache E-Tag...

For some DOS security we use CodeIgniter Filter like Throttle - to prevent too much connections in specific period. For example return http error 429 if connection count is more than 60 per minute. And other filters like check referrer, ip white/black list etc..

There is much more things, technics, design patterns & tricks to implement and do/fix & sometimes I feel that my whole life will be not enough to cover all those aspects xD

![Dashboard](https://raw.githubusercontent.com/alisacorporation/mmorpg-vuetify-admin-dashboard/master/2023-08-04_04-48_dashboard.png)

![Online](https://raw.githubusercontent.com/alisacorporation/mmorpg-vuetify-admin-dashboard/master/Screenshot_2023-08-11_12-15-57_online.png)

![Coins](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/Screenshot_2023-08-11_12-16-38_coins.png)

![Accounts](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-19_accounts.png)

![Characters](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-22_characters.png)

![Transfer Characters](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-25_transfer.png)

![Payments](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-27_payments.png)

![Events](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-29_events.png)

![Streams](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-30_streams.png)

![Errors](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-31_errors.png)

![Settings -> Servers](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-33_settings_servers.png)

![Agents](https://github.com/alisacorporation/mmorpg-vuetify-admin-dashboard/blob/master/2023-08-11_12-34_agents.png)
