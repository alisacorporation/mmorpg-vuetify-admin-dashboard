# Lineage 2 Interlude Admin Dashboard

### Project Overview

This project is an Admin Dashboard for the MMORPG game Lineage 2 Interlude, built using Vue.js 2 and Vuetify 2 for the frontend, with CodeIgniter 4 as the backend framework.

### Features
- #### User Management:
  - Signup
  - Password & Username Recovery
  - Change Password/Email
  - Unbind Characters by HWID (Hardware ID)
- #### Payment Systems:
  - Integration of over 10 payment systems developed over 2+ years
- #### Game Statistics and Rankings:
  - Top Characters, Clans, PK, PvP
  - Castle Attackers and Defenders
  - Character Search from Website
- #### Email Management:
  - SMTP Server Setup on Personal VPS (Docker) due to issues with commercial providers (high bounce rate from email verification policy)
  - Cost-effective solution at €6/month (4C/8G/200G SSD)
- #### Performance Optimization:
  - Browser Storage for API Responses (JSON encoding)
  - Fallback to File/Redis Cache if Browser Storage is Disabled
  - HTTP E-Tag for Efficient Data Transfers
- #### Security Measures:
  - Throttling (CodeIgniter Filter) to Prevent DoS Attacks (429 error for >60 requests/min)
  - Additional Security Filters: Referrer Check, IP Whitelist/Blacklist

### Technical Stack
- #### Frontend: 
  - Vue.js 2 
  - Vuetify 2
- #### Backend:
  - CodeIgniter 4 (REST API)
- #### Database: 
  - MySQL
- #### Deployment:
  - "deploy": "vite build && rsync -e 'ssh -p 40023' -avzP ./dist/* root@10.66.66.1:/var/www/html/example.com"

### Challenges and Solutions
- High Bounce Rate: Managed by transitioning to a self-hosted SMTP solution to accommodate our stringent user verification policies.
- Performance: Implemented efficient caching mechanisms to reduce server load and enhance user experience.

### Future Considerations
- Continuous improvement in user interface for better usability.
- Expansion of payment gateway options for global accessibility.
- Further security enhancements to combat evolving threats.

### Screenshots
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

### Contact
For inquiries or potential collaboration, please reach out at [your contact information].

This README now provides a clearer, more structured overview of your project, making it more appealing and informative for potential employers or collaborators. Remember to replace placeholders like [Database System] and [your contact information] with actual details.
