## OCBC

| Row | A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Project | Status | PM | Client | Stand in | Resources |
| 2 | OCBC SG | Help and support digital forms - Singpass V5 frontend deployment | Vanessa | Nisha | CatVu | [https://github.com/wearesection/ocbc-help-and-support-forms/pull/484](https://github.com/wearesection/ocbc-help-and-support-forms/pull/484) reverted in UAT hence need to revert revert again to bring back Singpass V5 codes |
| 3 | OCBC SG | Help and support digital forms - Phase 2 | Ai Yun | Nisha | CatVu | [https://github.com/wearesection/ocbc-help-and-support-forms/pull/491](https://github.com/wearesection/ocbc-help-and-support-forms/pull/491) included Singpass V5 <br>start with [https://ocbc-help-and-support-forms-491.hns-form.preview.wearesection.com/update_your_income_details/landing/](https://ocbc-help-and-support-forms-491.hns-form.preview.wearesection.com/update_your_income_details/landing/)  [https://app.asana.com/1/7545139225588/project/1208430808831702/task/1218233347356385?focus=true](https://app.asana.com/1/7545139225588/project/1208430808831702/task/1218233347356385?focus=true)  |
| 4 | OCBC BAU | SEO + GEO adjustments. Heading and CSS decoupling | Sihui | Hisham | Jack + Anthony | Need to restructure Heading style from main style. Evonne also has similar task. Can start to decouple the heading from our CSS eg. no more .class h2 { font-size: 22px }, should be .class { font-size: 22px }. add class name to the tag to change the font size. eg. &lt;h2 class="fz-22"&gt;  <br>[https://github.com/wearesection/ocbc-revamp-sg/pull/401](https://github.com/wearesection/ocbc-revamp-sg/pull/401)  |
| 5 | OCBC SG | Cards 2.0 flow - Telesales + Redirection + Popup content + Adjust's Smart script | Choiyee | Richard? | CatVu + Anthony | Mark Anthony build the logic in one Javascript, integrating into most of the cards pages.<br>Aqil built Telesales page and ported/upgraded Redirection page. |
| 6 | OCBC SG | Frank Referral | Unknown | Sundeep | CatVu | Update the script to provide pid value in the URL and share with the client in the email. The default qrcode is done in separate email |
| 7 | OCBC MY | Massive PDF clean up | Suen | Eileen | Jack | MY client wants to remove or redirect old PDF. <br>IT mention we can redirect ourselves, ask IT to point to us and how to redirect PDF.<br>Jack/Alvin to download the iwov pdf folder in OCBC laptop and use Sublime to search the list. <br>do the same for pages, download the sites folder in OCBC laptop and use Sublime to search the list. <br>share the list with Cat to use script to scan a) list of PDF in IW but not exist in any page &amp; b) list of PDF not in IW but exist in the page (probably PDF not found))   |
| 8 | OCBC HK | New path/workarea - Securities  | Tracy |  | Alvin |  |
| 9 | OCBC PPC Revamp | Page revamp + AA tagging | Tracy |  | Alvin + Anthony | Ask Zorba to bring over new files, dont overwrite any existing XML or DCR.  |
| 10 | Prudential eDM | new eDM project | Vanessa |  | CatVu | just pass to eDM dev team (Cody + MarkN) to build HTML |

## Braze

| Row | A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Project | Status | PM | Client | Stand in | Resources |
| 2 | CAG | Ongoing - BAU phase. <br>Using new template and content block (HTML for dynamic image slices) | Sherry | CRM team | Alvin | [https://dashboard-05.braze.com/](https://dashboard-05.braze.com/) |
| 3 | Chagee | Continue guiding the team to learn how to use Braze and IP warming | Akina | Cam Kang | CatVu | IP warming started on 6 Sept until 30 Sept.<br>[https://app.asana.com/1/7545139225588/project/830181490658972/task/1218219401172133?focus=true](https://app.asana.com/1/7545139225588/project/830181490658972/task/1218219401172133?focus=true) for IP warming schedule<br><br>[https://dashboard-07.braze.com/<br><br>](https://dashboard-07.braze.com/)Follow Braze IP Warming + Braze IP warming guide.PDF <br>Make sure to check the content and setup (enough volume to send) before launch. <br>After blast, check the delivery and bounce rate. Modify the segment filter if required<br><br>Just need help to launch and monitor until day 17 |
| 4 | CPT | Ongoing | Akina | Kimberly T | Nicholas Chew | Workbook and document: Section x CPT - Braze Onboarding Workbook (1) and CPT &lt;&gt; Braze Integration<br><br>AI analyzed and generated this CPT_Markets__Braze_Data_Model_Review_ENCN Can share it with CPT to begin their integration.<br><br>Follow the workbook, Data planning &gt; SDK integration &gt; Import users from CSV (less than 50mb) &gt; API or CDI to stream update into Braze<br><br>[https://dashboard-07.braze.com/](https://dashboard-07.braze.com/)  |
| 5 | Startrading | Just signed | Akina |  | Nicholas Chew |  |
| 6 | Challenger | Just signed | Akina |  | Nicholas Chew | Pre-sales POC done. |
| 7 | Esplanade | Just signed | Akina |  | Nicholas Chew | Sitecore is involved. If we need help there who can KY find |
| 8 | Fei Siong | Just signed | Akina |  | Nicholas Chew | Anthony to take on TA role |
| 9 | Disney Cruise Line | SFMC migration + Timeline and costing | Akina |  | Nicholas Chew | Q&amp;A |
| 10 | TANGS | POC with Snowflake | Akina |  | Nicholas Chew | Presented. Probably wait until 2027 |

## Other

| Row | A | B | C | D | E |
| --- | --- | --- | --- | --- | --- |
| 1 | Project | Hosting | PM/AM | Status | Next Step |
| 2 | SUTD Maintenance | WPVIP + GitHub | John S + Chloe | Analytic clean up. Vulnerability update. <br>UAT &gt; Preprod (1 approver) &gt; Production (2 approvers) | Huynh and Team taking over |
| 3 | SUTD Phase 3 | WPVIP + GitHub | John S + Chloe | P3A coming soon. Research Centres.  | Huynh and Team taking over |
| 4 | BankingCircle | Kinsta | Akina + Wawa | BAU. Reaching maxmium PHP Thread easily.  | Huynh and Team taking over |
| 5 | BandaiNamco | Vercel + Contentful + GitHub | Akina + Wawa | BAU. Becareful on embargoed content.  | Huynh and Team taking over |
| 6 | CMH | Cldy | John S + Chloe | No news | Huynh and Team taking over |
| 7 | Safco | Cldy | Vanessa | No retainer but recently has font license issue. CatVu handled this | Cat is looking at this |
| 8 | VirtuosGaming | Client own VPS | Akina + Wawa | BAU. Previously the folder was exposed, all sensitive (embargoed) assets are listed in directory. IT stated not bearing the responsibility. Becareful on embargoed content.  | Huynh and Team taking over |
| 9 | DollarAndSense | DigitalOcean | Liushuang + John P | Revamp status unknown + client wish to self serve on the advertisement placement.  | Huynh and Team taking over |
| 10 | Keppel | Azure | Vanessa | New project - Plot 6 using WhooshPro CMS | Cat is looking at this |
| 11 | SUSS - RFP |  |  |  | Cat is looking at this |
| 16 | Note: |  |  |  |  |
| 17 | SUTD WPVIP Support portal [https://support.wpvip.com/](https://support.wpvip.com/) |  |  |  |  |

## Internal Apps

| Row | A | B | C | D | E | F | G | H | I | J |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Application | IP | Hosting | Description | Usage | Remark | Requestor | Application Maintainer  | New Application Maintainer | Infra Plan (click to open) |
| 2 | Section Website | WPVIP | WPVIP | Section's account in WPVIP<br>[https://github.com/wpcomvip/section-agency-multisite-sandbox/](https://github.com/wpcomvip/section-agency-multisite-sandbox/) | Section main website - [https://wearesection.com/](https://wearesection.com/), |  | Ryan | Shawn + Anthony | Shawn + Anthony | Not in plan tab (out of scope) |
| 3 | The Kids | Vercel | Vercel | Section's account in Vercel<br>[https://github.com/wearesection/section-the_kids-2026](https://github.com/wearesection/section-the_kids-2026) | The Kids main website - [https://thekids.agency/](https://thekids.agency/) |  |  | Shawn + Anthony | Shawn + Anthony | Not in plan tab (out of scope) |
| 4 | Panel2 | 68.183.235.45 | Section DigitalOcean | [https://panel2.wearesection.com/](https://panel2.wearesection.com/) CloudPanel | [https://panel2.wearesection.com/](https://panel2.wearesection.com/) CloudPanel |  | Internal projects | Keei Yuan |  | Not in plan tab (out of scope) |
| 5 | Agents | 68.183.235.45 | Section DigitalOcean | [https://agents.cms.wearesection.com/home/workflows](https://agents.cms.wearesection.com/home/workflows) <br>n8n in Panel2 | [https://agents.cms.wearesection.com/home/workflows](https://agents.cms.wearesection.com/home/workflows) <br>n8n in Panel2 |  | Internal projects | Keei Yuan |  | Not in plan tab (out of scope) |
| 6 | GitHub Runner | 68.183.235.45 | Section DigitalOcean | maintain in Dockhands<br>[https://github.com/wearesection/section-github-runner](https://github.com/wearesection/section-github-runner) | maintain in Dockhands<br>[https://github.com/wearesection/section-github-runner](https://github.com/wearesection/section-github-runner) |  | Internal projects | Keei Yuan |  | Not in plan tab (out of scope) |
| 7 | Section VPN | 206.189.85.45 | Section DigitalOcean | [vpn.wearesection.com](http://vpn.wearesection.com/) Firezone (author not maintening) | VPN to SFTP &amp; SSH access 188.166.188.213 and other private network | Might have security issus on Firezone platform. Firezone is also protected by VPN | Aliff | Keei Yuan | Thomas  | [Keep and maintain → None](#gid=777000001&range=A9) |
| 8 | Section OCBC eDM Staging | 188.166.188.213 | Section DigitalOcean | All previews for pages or eDM mostly for OCBC<br>https://ocbc.ext1.wearesection.com <br>[https://ocbcmy.ext1.wearesection.com](https://ocbcmy.ext1.wearesection.com/) <br>[https://ospl.ext1.wearesection.com](https://ospl.ext1.wearesection.com/) <br>[https://ocbchk.ext1.wearesection.com](https://ocbchk.ext1.wearesection.com/) <br><br>Nginx based | All previews for pages or eDM mostly for OCBC<br>[https://ocbc.ext1.wearesection.com](https://ocbc.ext1.wearesection.com/) <br>[https://ocbcmy.ext1.wearesection.com](https://ocbcmy.ext1.wearesection.com/) <br>[https://ospl.ext1.wearesection.com](https://ospl.ext1.wearesection.com/) <br>[https://ocbchk.ext1.wearesection.com](https://ocbchk.ext1.wearesection.com/)  | NOTE:  188.166.188.213 is on Ubuntu 16 | Section CMS team + Section Suits + Section PM <br>for OCBC SG + MY + HK projects.  | Keei Yuan | Thomas  | Not in plan tab (out of scope) |
| 9 | Filesystem | 188.166.188.213 | RD DigitalOcean | [https://workspace.cms.wearesection.com/<br>](https://workspace.cms.wearesection.com/)[https://gitlab.com/ripplewerkzco/file-manager-laravel](https://gitlab.com/ripplewerkzco/file-manager-laravel) | Shared file manager for team assets. <br>Onboard user into this platform.  | NOTE:  188.166.188.213 is on Ubuntu 16 | CMS team + Implementation team<br> | Keei Yuan | Keei Yuan | [Relocate → New ubuntu 26 server](#gid=777000001&range=A12) |
| 10 | OCBC Promotion | 188.166.188.213 | RD DigitalOcean | [https://promo-sg.cms.wearesection.com/<br>http://promo-my.cms.wearesection.com/<br>](https://promo-sg.cms.wearesection.com/)https://gitlab.com/ripplewerkzco/card-promos-dashboard | Card promo dashboard for OCBC SG and MY | NOTE:  188.166.188.213 is on Ubuntu 16 | OCBC SG + MY projects | Keei Yuan | Keei Yuan | [Relocate → New ubuntu 26 server](#gid=777000001&range=A13) |
| 11 | Tracker | 188.166.188.213 | RD DigitalOcean | [https://tracker.cms.wearesection.com/<br>](https://tracker.cms.wearesection.com/)[https://gitlab.com/ripplewerkzco/ocbc-deployment-tracker](https://gitlab.com/ripplewerkzco/ocbc-deployment-tracker) | OCBC deployment tracking for staging and production releases + QRCode Generator | NOTE:  188.166.188.213 is on Ubuntu 16 | Tracy team use for QR code gen | Keei Yuan | Keei Yuan | [Remove, after conditions → New ubuntu 26 server](#gid=777000001&range=A14) |
| 12 | Order | 188.166.188.213 | Section DigitalOcean | [https://order.wearesection.com/](https://order.wearesection.com/) Laravel<br>[https://github.com/wearesection/section-drink-corner](https://github.com/wearesection/section-drink-corner) | [https://order.wearesection.com/](https://order.wearesection.com/) Laravel | NOTE:  188.166.188.213 is on Ubuntu 16<br> | Nid | Keei Yuan | Thomas  | [Relocate → New shared tools server](#gid=777000001&range=A15) |
| 13 | GlitchTip | 188.166.188.213 | Section DigitalOcean | Section DigitalOcean | Error and exception monitoring for internal hosted apps | NOTE:  188.166.188.213 is on Ubuntu 16 | Internal projects (For triage) | Keei Yuan |  | [Relocate → Should move to 235.45 server](#gid=777000001&range=A16) |
| 14 | GitHub Action - SFTP | 188.166.188.213 | RD DigitalOcean | [https://github.com/wearesection/sftp-remote<br>](https://github.com/wearesection/sftp-remote)use for OCBC SG CSL application upload to Staging server | Mostly uploads OCBC SG CSL builds to the staging server | NOTE:  188.166.188.213 is on Ubuntu 16 | OCBC SG CSL projects | Cat Vu |  | [Relocate → New ubuntu 26 server](#gid=777000001&range=A17) |
| 15 | Gitea | 188.166.188.213 | RD DigitalOcean | https://git.ext1.wearesection.com/<br>maintain in Dockhands. storing OCBC SG staging contents (HTML and assets inside specific folder) | Stores OCBC SG staging HTML and assets | NOTE:  188.166.188.213 is on Ubuntu 16 | Internal projects (For triage) | Keei Yuan |  | Not in plan tab (out of scope) |
| 16 | PR Preview | 188.166.188.213 | RD DigitalOcean | [https://preview.wearesection.com/](https://preview.wearesection.com/) GetMeli. <br>makintain in Dockhands. <br>Hosted multiple frontend websites. | [https://preview.wearesection.com/](https://preview.wearesection.com/) GetMeli. Hosted multiple frontend websites. | NOTE:  188.166.188.213 is on Ubuntu 16 | CSL and DEV team more | Keei Yuan |  | [Relocate → New ubuntu 26 server](#gid=777000001&range=A19) |
| 17 | RD VPN | 178.128.58.22 | RD DigitalOcean | [vpn.ripplewerkz.co](http://vpn.ripplewerkz.co/) Firezone (author not maintening) | VPN to SFTP &amp; SSH access 188.166.188.213  | Can consider removing. Usage currently is on Digital Ocean SSH and 188.166.188.213 | Can consider removing. Usage currently is on Digital Ocean SSH and 188.166.188.213 | Keei Yuan | N/A | [Remove, after conditions → None](#gid=777000001&range=A21) |
| 18 | Neuropsychiatry | 167.99.75.50 | Section DigitalOcean | [https://neuropsychiatry-associates.com/](https://neuropsychiatry-associates.com/) Nunjuck and PM2 <br>[https://github.com/wearesection/neuropsychiatry-associates/](https://github.com/wearesection/neuropsychiatry-associates/) | [https://neuropsychiatry-associates.com/](https://neuropsychiatry-associates.com/) Nunjuck and PM2 <br>[https://github.com/wearesection/neuropsychiatry-associates/](https://github.com/wearesection/neuropsychiatry-associates/) |  | neuropsychiatry-associates.<br>Tracy | Keei Yuan | Thomas  | [Remove, after conditions. Move to Vercel? → Stay on 167.99.75.50](#gid=777000001&range=A23) |
| 19 | Dockhands | 157.230.248.41 | Section DigitalOcean | [https://docker.cms.wearesection.com/stacks](https://docker.cms.wearesection.com/stacks) Dockhands (Portainer alternative) | Dockers management for a few servers.  |  | Internal projects | Keei Yuan |  | Not in plan tab (out of scope) |
| 20 | Panel1 | 157.230.248.41 | Section DigitalOcean | https://panel1.wearesection.com/  CloudPanel | CloudPanel to manage sites, SSL for Authentik, Dokku, Hotdesk, Inventory, GetOutline, Order |  | Internal projects | Keei Yuan |  | [Keep and maintain → Stay on Dockhand server](#gid=777000001&range=A26) |
| 21 | Inventory | 157.230.248.41 | Section DigitalOcean | [https://inventory.wearesection.com/](https://inventory.wearesection.com/) Snipe-IT | [https://inventory.wearesection.com/](https://inventory.wearesection.com/) Snipe-IT |  | Aliff | Keei Yuan |  | [Keep and maintain → Stay on Dockhand server](#gid=777000001&range=A27) |
| 22 | GetOutline | 157.230.248.41 | Section DigitalOcean | [http://my.wiki.wearesection.com/](http://my.wiki.wearesection.com/) and [https://wiki.gravitas.my/](https://wiki.gravitas.my/) maintain in Dockhands | [http://my.wiki.wearesection.com/](http://my.wiki.wearesection.com/) and [https://wiki.gravitas.my/](https://wiki.gravitas.my/) maintain in Dockhands |  | Aliff | Keei Yuan |  | Not in plan tab (out of scope) |
| 23 | Dokku | 157.230.248.41 | Section DigitalOcean | maintain in Dockhands similar to GetMeli. Hosted multiple web applications  | PaaS hosting for multiple internal web applications |  | Internal projects | Keei Yuan |  | [Relocate → Should move to .213](#gid=777000001&range=A30) |
| 24 | Authentik | 157.230.248.41 | Section DigitalOcean | [https://auth.wearesection.com/<br>](https://auth.wearesection.com/)maintain in Dockhands. Authentication and Authorization for internal applications | Single sign-on for internal applications.<br>Add user to group for custom authorization  |  | Interal projects.  | Keei Yuan |  | [Keep and maintain → Stay on Dockhand server](#gid=777000001&range=A31) |
| 25 | Hotdesk | 157.230.248.41 | Section DigitalOcean | [https://hotdesk.wearesection.com/<br>https://hotdesk.gravitas.my/<br>](https://hotdesk.wearesection.com/)maintain in Dockhands. Seatsurfing.  | Desk booking for SG and MY offices |  | Aliff | Keei Yuan |  | [Keep and maintain → Stay on Dockhand server](#gid=777000001&range=A32) |
| 26 | Browserless | 157.230.248.41 | Section DigitalOcean | [https://browserless.dokku.wearesection.com/<br>](https://browserless.dokku.wearesection.com/)maintain in Dockhands, used in n8n for CAG to screenshot for AI to validate content | Headless browser for n8n screenshot jobs |  | Changi + OCBC projects | Keei Yuan |  | [Relocate → Should move to 235.45](#gid=777000001&range=A33) |
| 27 | AStar Staging | 128.199.104.112 | RD DigitalOcean | Laravel | Laravel |  | Lionel | Keei Yuan |  | [Keep and maintain → ](#gid=777000001&range=A35) |
| 28 | OCBC SG CSL SSL certification | - | GoGetSSL | 2wayhandshake and digitalsignature between our staging environment and OCBC UAT environment | Buy 2 set of whitelisted SSL provider (GeoTrust TrueBusinessID), and upload one to our Docker volume and another to OCBC SG CSL team | Maybe transfer to Aliff | Client + CatVu | Keei Yuan |  | Not in plan tab (out of scope) |

## Restructuring Plan

| Row | A | B | C | D | E | F | G | H | I | J | K | L |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Application |  | Today (IP) | Action | Target | Contact first | Business Onwer | Application Onwership | Infrastructure owner | Secondary owner | Status |  |
| 2 | [Panel2 (Seciton's IMP Dev Apps)](https://panel2.wearesection.com/) | Section IMP Dev Server | 68.183.235.45 | Keep and maintain | Stay on Panel2 server as reverse proxy | Keei Yuan, Aliff | Keei Yuan / Cat Vu | Thomas | Thomas | Vinh |  |  |
| 3 | Agents (n8n - Managed by Dockhand) | Section IMP Dev Server | 68.183.235.45 | Keep and maintain | Managed by Dockhand | Keei Yuan, Aliff | Cat Vu / Keei Yuan | Thomas | Thomas | Vinh |  |  |
| 4 | Agent-2  | Section IMP Dev Server | 68.183.235.45 | Remove, after conditions | Managed by Dockhand |  | Cat Vu |  |  |  |  |  |
| 5 | Mongo | Section IMP Dev Server | 68.183.235.45 | Remove, after conditions | Managed by Dockhand |  | Cat Vu |  |  |  |  |  |
| 6 | Uptime | Section IMP Dev Server | 68.183.235.45 | Remove, after conditions | Managed by Dockhand |  | Cat Vu |  |  |  |  |  |
| 7 | GitHub Runner (Managed by Dockhand) | Section IMP Dev Server | 68.183.235.45 | Keep and maintain | Managed by Dockhand | Keei Yuan, Aliff | Cat Vu / Keei Yuan | Thomas | Thomas | Vinh |  |  |
| 9 | Section VPN | Section VPN | 206.189.85.45 | Keep and maintain | None | Aliff | Aliff | Thomas | Thomas | Vinh |  | - Consider in the future on how to move foward. |
| 11 | Section OCBC eDM Staging (Section's IMP Apps) | Section IMP OC Server | 188.166.188.213 | Relocate | New ubuntu 26 server | Keei Yuan, Cat Vu, Section CMS team | Tracy | Thomas | Thomas | Vinh |  |  |
| 12 | Filesystem | Section IMP OC Server | 188.166.188.213 | Relocate | New ubuntu 26 server | CMS and implementation teams | Tracy / Cat Vu | Keei Yuan | Thomas | Vinh |  |  |
| 13 | OCBC Promotion | Section IMP OC Server | 188.166.188.213 | Relocate | New ubuntu 26 server | OCBC SG and MY project teams | Tracy | Keei Yuan | Thomas | Vinh |  |  |
| 14 | Tracker | Section IMP OC Server | 188.166.188.213 | Remove, after conditions | New ubuntu 26 server | Tracy | Tracy | Keei Yuan | Thomas | Vinh |  |  |
| 15 | Order | Section IMP OC Server | 188.166.188.213 | Relocate | New shared tools server | Nid | Nid | Thomas | Thomas | Vinh |  |  |
| 16 | GlitchTip | Section IMP OC Server | 188.166.188.213 | Relocate | Should move to 235.45 server | Keei Yuan | Internal projects | Thomas | Thomas | Vinh |  |  |
| 17 | GitHub Action - SFTP | Section IMP OC Server | 188.166.188.213 | Relocate | New ubuntu 26 server | Cat Vu | OCBC SG CSL projects | Cat Vu | Thomas | Vinh |  |  |
| 18 | Gitea (Managed by Dockhand) | Section IMP OC Server | 188.166.188.213 | Relocate | New ubuntu 26 server | Keei Yuan | Internal projects | Keei Yuan | Thomas | Vinh |  |  |
| 19 | PR Preview | Section IMP OC Server | 188.166.188.213 | Relocate | New ubuntu 26 server | Cat Vu, dev team | Cat Vu / Keei Yuan | Keei Yuan | Thomas | Vinh |  |  |
| 21 | RD VPN |  | 178.128.58.22 | Remove, after conditions | None | Keei Yuan | Keei Yuan | N/A | Thomas | Vinh |  |  |
| 23 | Neuropsychiatry |  | 167.99.75.50 | Remove, after conditions. Move to Vercel? | Stay on 167.99.75.50 | Tracy | Tracy | Quan?? | Thomas | Vinh |  |  |
| 25 | [Dockhands (Section's Apps)](https://docker.cms.wearesection.com/) | Section Apps server | 157.230.248.41 | Keep and maintain | Stay on Dockhand server | Aliff | Thomas | Thomas | Thomas | Vinh |  |  |
| 26 | [Panel1](https://panel1.wearesection.com/) | Section Apps server | 157.230.248.41 | Keep and maintain | Stay on Dockhand server | Aliff | Keei Yuan / Cat Vu | Thomas?? | Thomas | Vinh |  |  |
| 27 | Inventory | Section Apps server | 157.230.248.41 | Keep and maintain | Stay on Dockhand server | Aliff - Will be deprovision after Aliff made it known to us | Aliff | Thomas | Thomas | Vinh |  |  |
| 28 | GetOutline (for MY) | Section Apps server | 157.230.248.41 | Keep and maintain | Stay on Dockhand server | Aliff | Aliff | Thomas | Thomas | Vinh |  |  |
| 29 | GetOutline (for SG) | Section Apps server | 157.230.248.41 | NEW | Stay on Dockhand server | Aliff | Aliff | Thomas | Thomas | Vinh |  |  |
| 30 | Dokku | Section Apps server | 157.230.248.41 | Relocate | Should move to .213 | Aliff | Cat Vu | Thomas | Thomas | Vinh |  |  |
| 31 | Authentik | Section Apps server | 157.230.248.41 | Keep and maintain | Stay on Dockhand server | Aliff | Thomas | Thomas | Thomas | Vinh |  |  |
| 32 | Hotdesk | Section Apps server | 157.230.248.41 | Keep and maintain | Stay on Dockhand server | Aliff | Aliff | Thomas | Thomas | Vinh |  |  |
| 33 | Browserless | Section Apps server | 157.230.248.41 | Relocate | Should move to 235.45 | Aliff | Changi + OCBC projects | Thomas | Thomas | Vinh |  |  |
| 35 | AStar Staging | Astart Staging | 128.199.104.112 | Keep and maintain |  | Lionel | Lionel | Yoga | Thomas | Vinh |  |  |
| 47 |  |  | Panel2 |  |  |  |  |  |  |  |  |  |

## To-do

| Row | A | B | C | D | E | F | G |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | # | Track | Action | Owner | Depends on | Status | Notes |
| 2 | A1 | A – Section's IMP Apps rebuild | Confirm whether Tracker, OCBC Promotion and Filesystem are still used | Tracy's team (Tracker); OCBC SG+MY (Promotion); CMS+implementation (Filesystem) | — | Open | Confirm to see if any of these doesn't need to exist on the new server |
| 3 | A2 | A – Section's IMP Apps rebuild | Size the new OCBC server's disk | Thomas | A1 | Open | If nothing is retired, old server uses 123 of 155 GB (79%) start at 250 GB for headroom, since disk only grows, never shrinks. |
| 4 | A3 | A – Section's IMP Apps rebuild | Confirm whether OCBC UAT whitelists the primary IP (188.166.188.213) or the Reserved IP (167.172.4.153) | Cat Vu | — | Open | Blocks the DNS/IP cutover step of A5 |
| 5 | A4 | A – Section's IMP Apps rebuild | Confirm whether PR Preview is used by clients other than OCBC | Cat Vu, Keei Yuan | — | Open | Low urgency, informs a later replace/retire decision, not the move itself |
| 6 | A5 | A – Section's IMP Apps rebuild | Execute the rebuild: provision the new Ubuntu 26.04 server, migrate apps app-by-app, cut over DNS | Thomas | A1, A2, A3 | Open | 6 steps: <br><br>(1) DO snapshot + file-level backup of Docker volumes/Gitea/Nginx config/SFTP users/cron/SSL certs, restore-tested on a spare droplet<br><br>(2) read-only inventory of the old server (containers, volumes, Nginx sites, open ports, SFTP users, every DNS name pointing at it), no changes yet <br><br>(3) build the new Ubuntu 26.04 server: start at 2 vCPU/4GB, OCBC-tagged DO project, firewall + key-only SSH, registered in Dockhand<br><br>(4) lower DNS TTL on affected hostnames a few days ahead so rollback is minutes, not hours<br><br>(5) move apps one at a time in order of risk, Gitea and PR Preview first (test via hosts-file override, then flip DNS), Section OCBC eDM Staging and the SFTP target last, after agreed with Cat Vu.<br><br>(6) keep the old server live 2 - 4 weeks as fallback, then power off, take a final snapshot, and only then destroy it. |
| 7 | B1 | B – RD VPN removal | Remove RD VPN's IP (178.128.58.22) from the 3 SSH allow-lists: Dockhand/Section VPN (port 3022), thelionsroar-bill (port 22), and Panel2 (port 22) | Thomas | — | Open | A few servers only accept SSH from a short list of trusted IPs (not from a person's laptop directly)<br><br>RD VPN's IP is on that list for Dockhand, Section VPN, thelionsroar-bill, and Panel2. <br><br>Section VPN's IP is already on all four, so removing RD VPN's entries is safe, nobody loses access. |
| 8 | B2 | B – RD VPN removal | Check the RD VPN box's authorized SSH keys/users directly and compare against who has keys on Section VPN | Thomas | B1 | Open | The one case that would actually break: if someone today reaches Dockhand/thelionsroar-bill/Panel2 only by hopping through RD VPN, they need Section VPN access added before RD VPN goes away. <br><br>Verify this directly off the box (authorized_keys, auth logs), needs SSH access to the RD VPN server first. |
| 9 | B3 | B – RD VPN removal | Remove the RD VPN | Thomas | B2 | Open | Agreed in the Oct 6 handover meeting: RD VPN has no other owner once SSH access is cleaned up (B1, B2). <br><br>Removing it only retires that VPN service, Section VPN is untouched and stays on Firezone (see C1). |
| 10 | C1 | C – Section VPN | Take over Firezone 0.8 maintenance (Thomas/Vinh): keep the WireGuard layer patched; no migration | Thomas, Vinh | — | Noted | Firezone 0.7 can't update to 1.x directly (different architecture), accepted the risk since it's protected by WireGuard. |
| 11 | C2 | C – Section VPN | Investigate what's causing slow network for some users on Section VPN (reported Oct 12, 2:21pm) and what to improve | Thomas | — | Open | Separate from the maintenance handover in C1 — this is a live performance complaint, not the Firezone-version decision. Check WireGuard throughput, VPN server load, and whether it's isolated to specific users/locations before concluding it's the VPN itself. |
| 12 | D1 | D – Shared-tools hosting | Decide Order and GlitchTip hosting: new shared-tools server, not Dockhand | Thomas | — | Open | Dockhand is $48/mo now (s-4vcpu-8gb), next tier up is s-8vcpu-16gb at $96/mo (+$48), shared by all 7 existing apps. <br><br>Suggestion: Cost-optimal way: a new s-1vcpu-2gb server at $12/mo, isolated just for Order + GlitchTip.<br><br>Purpose: To separate these app from OCBC server.  |
| 13 | E1 | E – Independent confirmations | Confirm AStar Staging's status and plan | Lionel | — | Open |  |
| 14 | F1 | F – Will do, later | Confirm who has DigitalOcean access to Section X Ripplewerkz but not the Section team, before moving Dockhand/Section VPN | Thomas, Aliff | — | Open | Same pattern as B2: moving these droplets to a different DO team could lock out anyone who only has console access to Section X Ripplewerkz, not Section. |
| 15 | F2 | F – Will do, later | Move Dockhand and the Section VPN into the Section team space | Thomas, Keei Yuan | B3, C1, F1 (ideally, not strictly) | Open | Separate, later decision; not part of this migration |

## Server Role and Sizing

| Row | A | B | C | D |
| --- | --- | --- | --- | --- |
| 1 | IP Address | Roles | Sizing | Space |
| 2 | 68.183.235.45 | Section IMP Dev Server |  |  |
| 3 | 206.189.85.45 | Section VPN |  |  |
| 4 | 188.166.188.213 | Section IMP OC Server |  |  |
| 5 | 167.99.75.50 / 157.230.248.41 | Section Apps server |  |  |
| 6 | 128.199.104.112 | Astart Staging |  |  |

## Server Role & Cost & Timeline

| Row | A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Monthly hosting cost |  |  |  |  |  |
| 2 | Item | Today | After migration | Change | Notes | Role |
| 3 | New OCBC server | - | $44 | $44 | s-2vcpu-4gb ($24) + ~200 GB volume (~$20) to reach the 250 GB disk target. DO list pricing, not re-verified this session — confirm in console. |  |
| 4 | New shared-tools server (Order + GlitchTip) | - | $12 | $12 | s-1vcpu-2gb — cost-optimal option from D1 |  |
| 5 | Old OCBC server (188.166.188.213) | $48 | - | ($48) | s-4vcpu-8gb-intel tier; deleted after the 2–4 week fallback window (A5). DO list pricing — confirm exact rate in console. |  |
| 6 | RD VPN (178.128.58.22) | $12 | - | ($12) | s-1vcpu-2gb; removed per B3. DO list pricing — confirm in console. |  |
| 7 | Dockhand | $48 | $48 | - | Unchanged — not resized (D1 recommends against it) |  |
| 8 | Section VPN | $12 | $12 | - | Unchanged — Firezone 0.8 retained, no migration (C1). DO list pricing — confirm in console. |  |
| 9 | Total | $120 | $116 | ($4) |  |  |
| 11 | Timeline (10 weeks, 0.1 FTE each for Thomas and Vinh) |  |  |  |  |  |
| 12 | Phase | Weeks | Done when |  |  |  |
| 13 | Get access | 1–2 | Thomas and Vinh can log in everywhere |  |  |  |
| 14 | Discovery | 2–4 | Every app in the decision table has a usage answer |  |  |  |
| 15 | Migration waves | 4–9 | Every kept app runs on its new server |  |  |  |
| 16 | Cleanup | 9–10 | Old server deleted |  |  |  |

