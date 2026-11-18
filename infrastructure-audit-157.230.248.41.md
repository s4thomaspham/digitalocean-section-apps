## Overview

| Row | A | B | C |
| --- | --- | --- | --- |
| 1 | VM inspection and owner review |  |  |
| 4 | Topic | Current finding / next step | Scope or evidence |
| 5 | What this workbook is for | I inspected this VM and listed what I found. The next step is to confirm each item with its owner. | Inventory first, owner confirmation second, cleanup proposal third. |
| 6 | VM inspected | 157.230.248.41 / internal-tools-v1 | Read-only SSH audit on 17 Nov 2026, approximately 13:33–13:40 ICT. |
| 7 | Host resources | Ubuntu 22.04; 4 CPUs; approximately 7.8 GiB RAM | Host reported as running on KVM. |
| 8 | Root disk | 155 GB total; 113 GB used; 42 GB free; 73% used | No per-application storage analysis was performed. |
| 9 | What is running here | Docker workloads, Dokku and Nginx | Running status does not confirm ongoing business use. |
| 10 | Configured traffic flow | Domain → host Nginx → Dokku :4080/:4443 → application | Configuration observed; DNS and end-to-end service health not verified. |
| 11 | Other configured flow | Domain → host Nginx → individual service port | Wiki, desk booking, SSO, Browserless and monitoring routes. |
| 12 | VM Inventory | One entry per workload observed, with image, status, ports and likely purpose. | Purpose is inferred from name/image and must be confirmed. |
| 13 | Domain Routes | Nginx route inventory and configured upstreams. | This is not an export of the company's DNS records. |
| 14 | Review Steps | The order to inspect, confirm ownership and propose changes. | Implementation requires separate approval after a concrete proposal. |
| 15 | Evidence | Audit notes and limitations. | Full DigitalOcean account, DNS zones, usage and backups remain unverified. |

## VM Inventory

| Row | A | B | C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | What I found on this VM |  |  |  |  |  |  |  |
| 4 | Item ID | Workload name / audit label | Purpose / usage (see evidence) | Image | Observed status | Recorded ports | Owner | Next action |
| 5 | APP-01 | ocbc-sff-digital-2026.web.1 | Project application | dokku/ocbc-sff-digital-2026:latest | Up healthy | 3000/tcp | To be confirmed | Identify and confirm owner |
| 6 | APP-02 | keppel-plot6.web.1 | Project application | dokku/keppel-plot6:latest | Up healthy | 4080/tcp | To be confirmed | Identify and confirm owner |
| 7 | APP-03 | mongo ocbc-sff-digital-2026-db | Database / cache | mongo:8.2.9 | Up | 27017/tcp | To be confirmed | Identify and confirm owner |
| 8 | APP-04 | Outline SG (audit label) | Internal wiki; SG/MY-to-port mapping needs confirmation. | outline:latest | Up healthy | 5000-&gt;3000 | To be confirmed | Identify and confirm owner |
| 9 | APP-05 | Outline MY (audit label) | Internal wiki; SG/MY-to-port mapping needs confirmation. | outline:latest | Up healthy | 5001-&gt;3000 | To be confirmed | Identify and confirm owner |
| 10 | APP-06 | my-getoutline-postgres-1 | Database / cache | postgres:18 | Up healthy | 5432/tcp | To be confirmed | Identify and confirm owner |
| 11 | APP-07 | my-getoutline-redis-1 | Database / cache | redis | Up healthy | 6379/tcp | To be confirmed | Identify and confirm owner |
| 12 | APP-08 | ocbc-csl-api.web.1 | Project API | dokku/ocbc-csl-api:latest | Up 2w | none | To be confirmed | Identify and confirm owner |
| 13 | APP-09 | dokku.mongo.bypasscors | Database / cache | mongo:8.2.9 | Up 2w | 27017/tcp | To be confirmed | Identify and confirm owner |
| 14 | APP-10 | staff-digital-wealth-day.web.1 | Project application | dokku/staff-digital-wealth-day:latest | Up healthy | 3000/tcp | To be confirmed | Identify and confirm owner |
| 15 | APP-11 | pru-fa.web.1 | Project application | dokku/pru-fa:latest | Up 2w | 80,443,43554/tcp | To be confirmed | Identify and confirm owner |
| 16 | APP-12 | ocbc-sff-digital-prototype.web.1 | Prototype / demo | dokku/ocbc-sff-digital-prototype:latest | Up healthy | 3000/tcp | To be confirmed | Confirm lifecycle and usage |
| 17 | APP-13 | dokku.mongo.ocbc-sff-prototype | Database / cache | mongo:8.0.13 | Up 2w | 27017/tcp | To be confirmed | Confirm lifecycle and usage |
| 18 | APP-14 | ocbc-moa-prototype.web.1 | Prototype / demo | dokku/ocbc-moa-prototype:latest | Up 2w | 3000/tcp | To be confirmed | Confirm lifecycle and usage |
| 19 | APP-15 | edm-generator.web.1 | EDM generation | dokku/edm-generator:latest | Up 2w | 3000/tcp | To be confirmed | Identify and confirm owner |
| 20 | APP-16 | utcors-proxy.web.1 | Project application | dokku/utcors-proxy:latest | Up 2w | 8080/tcp | To be confirmed | Identify and confirm owner |
| 21 | APP-17 | browserless | Headless browser for n8n screenshots, including CAG content validation; Changi/OCBC projects listed. | [ghcr.io/browserless/chromium:latest](http://ghcr.io/browserless/chromium:latest) | Up 2w | 6000-&gt;3000/tcp | To be confirmed | Identify and confirm owner |
| 22 | APP-18 | seatsurfing-server-1 | Seatsurfing desk booking for SG and MY offices. | seatsurfing/backend | Up healthy | 7070-&gt;8080/tcp | To be confirmed | Identify and confirm owner |
| 23 | APP-19 | seatsurfing-db-1 | Desk booking | postgres:16 | Up 2w | 5432/tcp | To be confirmed | Identify and confirm owner |
| 24 | APP-20 | countdown-demo.web.1 | Prototype / demo | dokku/countdown-demo:latest | Up 2w | 5000/tcp | To be confirmed | Confirm lifecycle and usage |
| 25 | APP-21 | authentik-server-1 | SSO and group-based authorization for internal applications. | [ghcr.io/goauthentik/server:2026.5.0](http://ghcr.io/goauthentik/server:2026.5.0) | Up healthy | 7080-&gt;9000,7443-&gt;9443 | To be confirmed | Identify and confirm owner |
| 26 | APP-22 | authentik-worker-1 | Authentication / SSO | [ghcr.io/goauthentik/server:2026.5.0](http://ghcr.io/goauthentik/server:2026.5.0) | Up healthy | no ports | To be confirmed | Identify and confirm owner |
| 27 | APP-23 | authentik-redis-1 | Database / cache | redis:alpine | Up healthy | 6379/tcp | To be confirmed | Identify and confirm owner |
| 28 | APP-24 | authentik-postgresql-1 | Database / cache | postgres:12-alpine | Up healthy | no ports | To be confirmed | Identify and confirm owner |
| 29 | APP-25 | authentik-postgresql_16-1 | Database / cache | postgres:16-alpine | Up healthy | 5432/tcp | To be confirmed | Identify and confirm owner |
| 30 | APP-26 | dockhand-dockhand-1 | Docker management across several servers. | fnsys/dockhand:latest | Up healthy | 9443-&gt;3000 | To be confirmed | Identify and confirm owner |
| 31 | APP-27 | dockhand-postgres-1 | Database / cache | 87e04d274d18 | Up 2w | 5432/tcp | To be confirmed | Identify and confirm owner |
| 32 | APP-28 | dokku | PaaS hosting multiple internal web applications. | dokku/dokku:0.37.6 | Up 2w | 3022-&gt;22,4080-&gt;80,4443-&gt;443 | To be confirmed | Identify and confirm owner |
| 33 | APP-29 | statping | Monitoring | adamboutcher/statping-ng | Up healthy | 5080-&gt;8080 | To be confirmed | Identify and confirm owner |
| 34 | APP-30 | node-exporter | Monitoring | prom/node-exporter:latest | Up 2w | 9100-&gt;9100 | To be confirmed | Identify and confirm owner |
| 35 | APP-31 | portainer_agent | Deployment / administration | 7694bd834ce7 | Up 2w | 9001-&gt;9001 | To be confirmed | Identify and confirm owner |
| 36 | APP-32 | dokku.mongo.wealth-day-db | Database / cache | mongo:8.0.13 | Up 2w | 27017/tcp | To be confirmed | Identify and confirm owner |
| 37 | APP-33 | dokku.mongo.edm-generator-db | Database / cache | mongo:8.0.13 | Up 2w | 27017/tcp | To be confirmed | Identify and confirm owner |
| 38 | APP-34 | seatsurfing-admin-ui-1 | Desk booking | 4b70b5b2af35 | Up 2w | 3000/tcp | To be confirmed | Identify and confirm owner |
| 39 | APP-35 | seatsurfing-booking-ui-1 | Desk booking | 4105231eaa91 | Up 2w | 3001/tcp | To be confirmed | Identify and confirm owner |
| 40 | APP-36 | raise-storybook.web.1 | UI component preview | dokku/raise-storybook:latest | Up 2w | none | To be confirmed | Confirm lifecycle and usage |
| 41 | APP-37 | download-pdfs-from-url.web.1 | Project application | dokku/download-pdfs-from-url:latest | Up 2w | none | To be confirmed | Identify and confirm owner |
| 42 | APP-38 | dokku.mongo.ocbc-moa-prototype | Database / cache | mongo:8.0.13 | Up 2w | 27017/tcp | To be confirmed | Confirm lifecycle and usage |
| 43 | APP-39 | section-website-prod.web.1 | VM workload role unconfirmed; main website documented on WPVIP. | dokku/section-website-prod:latest | Up 2w | 3000/tcp | To be confirmed | Identify and confirm owner |
| 44 | APP-40 | section-website-staging.web.1 | VM workload role unconfirmed; main website documented on WPVIP. | dokku/section-website-staging:latest | Up 2w | 3000/tcp | To be confirmed | Confirm lifecycle and usage |
| 45 | APP-41 | section-dashboard.web.1 | Project application | dokku/section-dashboard:latest | Up 2w | 3001/tcp | To be confirmed | Identify and confirm owner |
| 46 | APP-42 | ocbc-eco-api.web.1 | Project API | dokku/ocbc-eco-api:latest | Up 2w | none | To be confirmed | Identify and confirm owner |
| 47 | APP-43 | section-namecard-api.web.1 | Project API | dokku/section-namecard-api:latest | Up 2w | 3000/tcp | To be confirmed | Identify and confirm owner |
| 48 | APP-44 | section-hello.web.1 | Project application | dokku/section-hello:latest | Up 2w | 3000/tcp | To be confirmed | Identify and confirm owner |
| 49 | APP-45 | ocbc-oa-vendor-api.web.1 | Project API | dokku/ocbc-oa-vendor-api:latest | Up 2w | none | To be confirmed | Identify and confirm owner |
| 50 | APP-46 | ocbc-mb-life-goals-mock-api.web.1 | Prototype / demo | dokku/ocbc-mb-life-goals-mock-api:latest | Up 2w | none | To be confirmed | Confirm lifecycle and usage |
| 51 | APP-47 | resource-soketi | Realtime WebSocket service | [quay.io/soketi/soketi:1.4-16-debian](http://quay.io/soketi/soketi:1.4-16-debian) | Up 2w | 6002-&gt;6001,9602-&gt;9601 | To be confirmed | Identify and confirm owner |
| 52 | APP-48 | order-soketi | Realtime WebSocket service | [quay.io/soketi/soketi:1.4-16-debian](http://quay.io/soketi/soketi:1.4-16-debian) | Up 2w | 6001-&gt;6001,9601-&gt;9601 | To be confirmed | Identify and confirm owner |

## Domain Routes

| Row | A | B | C | D | E | F | G |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Domain routes found in Nginx |  |  |  |  |  |  |
| 4 | Route ID | Name from Nginx config | Configured upstream / port | Route type | Recorded directives | DNS / live check | Owner |
| 5 | DOM-01 | [auth1.wearesection.com](http://auth1.wearesection.com) | 6443,5443 | Direct service port | auth1.wearesection.com; root /home/wearesection-auth1/...; proxy_pass 6443,5443. | Not checked | To be confirmed |
| 6 | DOM-02 | [auth.ripplewerkz.co](http://auth.ripplewerkz.co) | 7080 | Direct service port | auth.ripplewerkz.co; root /home/ripplewerkz-auth/...; proxy_pass 7080. | Not checked | To be confirmed |
| 7 | DOM-03 | [auth.wearesection.com](http://auth.wearesection.com) | [https://127.0.0.1:7443](https://127.0.0.1:7443) | Direct service port | auth.wearesection.com; root /home/wearesection-auth/...; proxy_pass https://127.0.0.1:7443. | Not checked | To be confirmed |
| 8 | DOM-04 | [bc.ext2.wearesection.com](http://bc.ext2.wearesection.com) | 8080 | Direct service port | bc.ext2.wearesection.com; root .../public; proxy_pass 8080. | Not checked | To be confirmed |
| 9 | DOM-05 | [beta-v1.wearesection.com](http://beta-v1.wearesection.com) | 4080 | Via Dokku | beta-v1.wearesection.com; root /home/wearesection-beta-v1/...; proxy_pass 4080. | Not checked | To be confirmed |
| 10 | DOM-06 | [browserless.dokku.wearesection.com](http://browserless.dokku.wearesection.com) | 6000 | Direct service port | browserless.dokku.wearesection.com; proxy_pass 6000. | Not checked | To be confirmed |
| 11 | DOM-07 | [cfssff.com](http://cfssff.com) | 4080 | Via Dokku | www.cfssff.com/cfssff.com/www1.cfssff.com; proxy_pass 4080. | Not checked | To be confirmed |
| 12 | DOM-08 | [countdown-demo.dokku.wearesection.com](http://countdown-demo.dokku.wearesection.com) | 4080 | Via Dokku | countdown-demo.dokku.wearesection.com; proxy_pass 4080. | Not checked | To be confirmed |
| 13 | DOM-09 | custom-domain | [https://127.0.0.1:8443/](https://127.0.0.1:8443/) | Direct service port | panel1.wearesection.com; root /home/clp/htdocs/app/files/public; proxy_pass https://127.0.0.1:8443/. | Not checked | To be confirmed |
| 14 | DOM-10 | default | No proxy_pass recorded | Root/static or unresolved route | server_name _; listen 80/443 default_server. | Not checked | To be confirmed |
| 15 | DOM-11 | [docker.cms.wearesection.com](http://docker.cms.wearesection.com) | 9443 | Direct service port | docker.cms.wearesection.com; proxy_pass 9443. | Not checked | To be confirmed |
| 16 | DOM-12 | [dokku.wearesection.com](http://dokku.wearesection.com) | [https://127.0.0.1:4443](https://127.0.0.1:4443) | Via Dokku | dokku.wearesection.com; proxy_pass https://127.0.0.1:4443. | Not checked | To be confirmed |
| 17 | DOM-13 | [download-pdfs-from-url.dokku.wearesection.com](http://download-pdfs-from-url.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 18 | DOM-14 | [dozz.ripplewerkz.co](http://dozz.ripplewerkz.co) | 8090 | Direct service port | dozz.ripplewerkz.co; proxy_pass 8090. | Not checked | To be confirmed |
| 19 | DOM-15 | [edm-generator.dokku.wearesection.com](http://edm-generator.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 20 | DOM-16 | [gcmd.ext2.wearesection.com](http://gcmd.ext2.wearesection.com) | 8080 | Direct service port | gcmd.ext2.wearesection.com; root ...; proxy_pass 8080. | Not checked | To be confirmed |
| 21 | DOM-17 | [hhmw.ext2.wearesection.com](http://hhmw.ext2.wearesection.com) | No proxy_pass recorded | Root/static or unresolved route | hhmw.ext2.wearesection.com; root /home/wearesection-hhmw-ext2/... | Not checked | To be confirmed |
| 22 | DOM-18 | [hotdesk.gravitas.my](http://hotdesk.gravitas.my) | 7070 | Direct service port | hotdesk.gravitas.my; proxy_pass 7070. | Not checked | To be confirmed |
| 23 | DOM-19 | [hotdesk.wearesection.com](http://hotdesk.wearesection.com) | 7070 | Direct service port | hotdesk.wearesection.com; proxy_pass 7070. | Not checked | To be confirmed |
| 24 | DOM-20 | [inventory.wearesection.com](http://inventory.wearesection.com) | No proxy_pass recorded | Root/static or unresolved route | inventory.wearesection.com; root .../public. | Not checked | To be confirmed |
| 25 | DOM-21 | [keppel-plot6.dokku.wearesection.com](http://keppel-plot6.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 26 | DOM-22 | [my.wiki.wearesection.com](http://my.wiki.wearesection.com) | 5000 | Direct service port | my.wiki.wearesection.com; proxy_pass 5000. | Not checked | To be confirmed |
| 27 | DOM-23 | [ocbc-csl-api.dokku.wearesection.com](http://ocbc-csl-api.dokku.wearesection.com) | [https://127.0.0.1:4443](https://127.0.0.1:4443) | Via Dokku | domain same; proxy_pass https://127.0.0.1:4443. | Not checked | To be confirmed |
| 28 | DOM-24 | [ocbc-eco-api.dokku.wearesection.com](http://ocbc-eco-api.dokku.wearesection.com) | [https://127.0.0.1:4443](https://127.0.0.1:4443) | Via Dokku | domain same; proxy_pass https://127.0.0.1:4443. | Not checked | To be confirmed |
| 29 | DOM-25 | [openapi-hs-cussec.wearesection.com](http://openapi-hs-cussec.wearesection.com) | 1081 | Direct service port | domain same; proxy_pass 1081. | Not checked | To be confirmed |
| 30 | DOM-26 | [openapi-hs-form.wearesection.com](http://openapi-hs-form.wearesection.com) | 1080 | Direct service port | domain same; proxy_pass 1080. | Not checked | To be confirmed |
| 31 | DOM-27 | [order.wearesection.com](http://order.wearesection.com) | 6001,8080 | Direct service port | order.wearesection.com; root .../public; proxy_pass 6001,8080. | Not checked | To be confirmed |
| 32 | DOM-28 | [prototype-one.dokku.wearesection.com](http://prototype-one.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 33 | DOM-29 | [prototype-two.dokku.wearesection.com](http://prototype-two.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 34 | DOM-30 | [pru-fa.dokku.wearesection.com](http://pru-fa.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 35 | DOM-31 | [raise-storybook.dokku.wearesection.com](http://raise-storybook.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 36 | DOM-32 | [resource.wearesection.com](http://resource.wearesection.com) | 8080,6002 | Direct service port | resource.wearesection.com; root .../public; proxy_pass 8080,6002. | Not checked | To be confirmed |
| 37 | DOM-33 | [sccb.ext2.wearesection.com](http://sccb.ext2.wearesection.com) | No proxy_pass recorded | Root/static or unresolved route | sccb.ext2.wearesection.com; root /home/wearesection-sccb-ext2/... | Not checked | To be confirmed |
| 38 | DOM-34 | [section-dashboard.dokku.wearesection.com](http://section-dashboard.dokku.wearesection.com) | 4080, 4080/verify, 4080/profile | Via Dokku | server_name section-dashboard; proxy_pass 4080, 4080/verify, 4080/profile. | Not checked | To be confirmed |
| 39 | DOM-35 | [section-hello.dokku.wearesection.com](http://section-hello.dokku.wearesection.com) | 4080, 4080/verify, 4080/profile | Via Dokku | server_name section-hello; proxy_pass 4080, 4080/verify, 4080/profile. | Not checked | To be confirmed |
| 40 | DOM-36 | [section-namecard-api.dokku.wearesection.com](http://section-namecard-api.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 41 | DOM-37 | [section-website-prod.dokku.wearesection.com](http://section-website-prod.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 42 | DOM-38 | [smu-blog.ext2.wearesection.com](http://smu-blog.ext2.wearesection.com) | No proxy_pass recorded | Root/static or unresolved route | wildcard + smu-blog.ext2.wearesection.com; root .../web. | Not checked | To be confirmed |
| 43 | DOM-39 | [smu-staging.ext2.wearesection.com](http://smu-staging.ext2.wearesection.com) | No proxy_pass recorded | Root/static or unresolved route | smu-staging.ext2.wearesection.com; root .../web. | Not checked | To be confirmed |
| 44 | DOM-40 | [sph.ext2.wearesection.com](http://sph.ext2.wearesection.com) | No proxy_pass recorded | Root/static or unresolved route | sph.ext2.wearesection.com; root /home/wearesection-sph-ext2/... | Not checked | To be confirmed |
| 45 | DOM-41 | [uptime.ripplewerkz.co](http://uptime.ripplewerkz.co) | 5080 | Direct service port | uptime.ripplewerkz.co; proxy_pass 5080. | Not checked | To be confirmed |
| 46 | DOM-42 | [utcors-proxy.dokku.wearesection.com](http://utcors-proxy.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 47 | DOM-43 | [wealth-day.dokku.wearesection.com](http://wealth-day.dokku.wearesection.com) | 4080 | Via Dokku | domain same; proxy_pass 4080. | Not checked | To be confirmed |
| 48 | DOM-44 | [wiki.gravitas.my](http://wiki.gravitas.my) | 5001 | Direct service port | wiki.gravitas.my; proxy_pass 5001. | Not checked | To be confirmed |

## Evidence

| Row | A | B |
| --- | --- | --- |
| 1 | Audit evidence and scope |  |
| 4 | Reference / topic | Evidence |
| 5 | Scope | Single VM: 157.230.248.41 |
| 6 | Approximate labels | Outline SG/MY and mongo ocbc-sff-digital-2026-db are labels recorded during the audit. |
| 7 | Old directory labels | gcmd-ext2, bc-ext2, smu-blog-ext2 and smu-staging-ext2 were reported with .old suffixes. |
| 8 | E-001 | Docker rows: staff-digital-wealth-day.web.1&#124;dokku/staff-digital-wealth-day:latest&#124;Up 2w healthy&#124;3000/tcp |
| 9 | E-002 | Docker rows: pru-fa.web.1&#124;dokku/pru-fa:latest&#124;Up 2w&#124;80,443,43554/tcp |
| 10 | E-003 | Docker rows: ocbc-sff-digital-prototype.web.1&#124;dokku/ocbc-sff-digital-prototype:latest&#124;Up 2w healthy&#124;3000/tcp |
| 11 | E-004 | Docker rows: dokku.mongo.ocbc-sff-prototype&#124;mongo:8.0.13&#124;Up 2w&#124;27017/tcp |
| 12 | E-005 | Docker rows: ocbc-moa-prototype.web.1&#124;dokku/ocbc-moa-prototype:latest&#124;Up 2w&#124;3000/tcp |
| 13 | E-006 | Docker rows: edm-generator.web.1&#124;dokku/edm-generator:latest&#124;Up 2w&#124;3000/tcp; utcors-proxy.web.1&#124;dokku/utcors-proxy:latest&#124;Up 2w&#124;8080/tcp |
| 14 | E-007 | Docker rows: browserless&#124;ghcr.io/browserless/chromium:latest&#124;Up 2w&#124;6000-&gt;3000/tcp |
| 15 | E-008 | Docker rows: seatsurfing-server-1&#124;seatsurfing/backend&#124;Up 2w healthy&#124;7070-&gt;8080/tcp; seatsurfing-db-1&#124;postgres:16&#124;Up 2w&#124;5432/tcp |
| 16 | E-009 | Docker rows: countdown-demo.web.1&#124;dokku/countdown-demo:latest&#124;Up 2w&#124;5000/tcp |
| 17 | E-010 | Docker rows: authentik-server/worker&#124;ghcr.io/goauthentik/server:2026.5.0&#124;Up 2w healthy; server 7080-&gt;9000,7443-&gt;9443 |
| 18 | E-011 | Docker rows: authentik-redis-1&#124;redis:alpine&#124;Up 2w healthy&#124;6379/tcp; authentik-postgresql-1&#124;postgres:12-alpine&#124;Up 2w healthy |
| 19 | E-012 | Docker rows: authentik-postgresql_16-1&#124;postgres:16-alpine&#124;Up 2w healthy&#124;5432/tcp |
| 20 | E-013 | Docker rows: dockhand-dockhand-1&#124;fnsys/dockhand:latest&#124;Up 2w healthy&#124;9443-&gt;3000; dockhand-postgres-1&#124;87e04d274d18&#124;Up 2w&#124;5432 |
| 21 | E-014 | Docker rows: dokku&#124;dokku/dokku:0.37.6&#124;Up 2w&#124;3022-&gt;22,4080-&gt;80,4443-&gt;443 |
| 22 | E-015 | Docker rows: statping&#124;adamboutcher/statping-ng&#124;Up 2w healthy&#124;5080-&gt;8080; node-exporter&#124;prom/node-exporter:latest&#124;Up 2w&#124;9100 |
| 23 | E-016 | Docker rows: portainer_agent&#124;7694bd834ce7&#124;Up 2w&#124;9001-&gt;9001; dokku.mongo.wealth-day-db&#124;mongo:8.0.13&#124;Up 2w&#124;27017 |
| 24 | E-017 | Docker rows: dokku.mongo.edm-generator-db&#124;mongo:8.0.13&#124;Up 2w&#124;27017; seatsurfing-admin-ui-1&#124;4b70b5b2af35&#124;Up 2w&#124;3000/tcp |
| 25 | E-018 | Docker rows: seatsurfing-booking-ui-1&#124;4105231eaa91&#124;Up 2w&#124;3001/tcp; raise-storybook.web.1&#124;dokku/raise-storybook:latest&#124;Up 2w&#124;ports none |
| 26 | E-019 | Docker rows: download-pdfs-from-url.web.1&#124;dokku/download-pdfs-from-url:latest&#124;Up 2w&#124;ports none |
| 27 | E-020 | Docker rows: dokku.mongo.ocbc-moa-prototype&#124;mongo:8.0.13&#124;Up 2w&#124;27017/tcp |
| 28 | E-021 | Docker rows: section-website-prod.web.1&#124;dokku/section-website-prod:latest&#124;Up 2w&#124;3000/tcp |
| 29 | E-022 | Docker rows: section-website-staging.web.1&#124;dokku/section-website-staging:latest&#124;Up 2w&#124;3000/tcp |
| 30 | E-023 | Docker rows: section-dashboard.web.1&#124;dokku/section-dashboard:latest&#124;Up 2w&#124;3001/tcp |
| 31 | E-024 | Docker rows: ocbc-eco-api.web.1&#124;dokku/ocbc-eco-api:latest&#124;Up 2w&#124;ports none |
| 32 | E-025 | Host internal-tools-v1; Ubuntu 22.04; CPU 4; RAM 8127916 kB (~7.75 GiB), via hostname/nproc/proc/meminfo. |
| 33 | E-026 | Disk df -h /: /dev/vda1 155G total, 113G used, 42G free (73%). |
| 34 | E-027 | qm, pct, virsh unavailable by command -v. |
| 35 | E-028 | SSH BatchMode=yes StrictHostKeyChecking=yes ConnectTimeout=12 to root@157.230.248.41. |
| 36 | E-029 | Docker: ocbc-sff-digital-2026.web.1&#124;dokku/ocbc-sff-digital-2026:latest&#124;Up healthy&#124;3000/tcp |
| 37 | E-030 | Docker: keppel-plot6.web.1&#124;dokku/keppel-plot6:latest&#124;Up healthy&#124;4080/tcp |
| 38 | E-031 | Docker: mongo ocbc-sff-digital-2026-db&#124;mongo:8.2.9&#124;Up&#124;27017/tcp |
| 39 | E-032 | Docker: Outline SG&#124;outline:latest&#124;Up healthy&#124;5000-&gt;3000; MY&#124;outline:latest&#124;Up healthy&#124;5001-&gt;3000 |
| 40 | E-033 | Docker: my-getoutline-postgres-1&#124;postgres:18&#124;Up healthy&#124;5432/tcp |
| 41 | E-034 | Docker: my-getoutline-redis-1&#124;redis&#124;Up healthy&#124;6379/tcp |
| 42 | E-035 | Docker: ocbc-csl-api.web.1&#124;dokku/ocbc-csl-api:latest&#124;Up 2w&#124;none |
| 43 | E-036 | Docker: dokku.mongo.bypasscors&#124;mongo:8.2.9&#124;Up 2w&#124;27017/tcp |
| 44 | E-037 | Docker: staff-digital-wealth-day.web.1&#124;dokku/staff-digital-wealth-day:latest&#124;Up healthy&#124;3000/tcp |
| 45 | E-038 | Docker: pru-fa.web.1&#124;dokku/pru-fa:latest&#124;Up 2w&#124;80,443,43554/tcp |
| 46 | E-039 | Docker: ocbc-sff-digital-prototype.web.1&#124;dokku/ocbc-sff-digital-prototype:latest&#124;Up healthy&#124;3000/tcp |
| 47 | E-040 | Docker: dokku.mongo.ocbc-sff-prototype&#124;mongo:8.0.13&#124;Up 2w&#124;27017/tcp |
| 48 | E-041 | Docker: ocbc-moa-prototype.web.1&#124;dokku/ocbc-moa-prototype:latest&#124;Up 2w&#124;3000/tcp |
| 49 | E-042 | Docker: edm-generator.web.1&#124;dokku/edm-generator:latest&#124;Up 2w&#124;3000/tcp |
| 50 | E-043 | Docker: utcors-proxy.web.1&#124;dokku/utcors-proxy:latest&#124;Up 2w&#124;8080/tcp |
| 51 | E-044 | Docker: browserless&#124;ghcr.io/browserless/chromium:latest&#124;Up 2w&#124;6000-&gt;3000/tcp |
| 52 | E-045 | Docker: seatsurfing-server-1&#124;seatsurfing/backend&#124;Up healthy&#124;7070-&gt;8080/tcp |
| 53 | E-046 | Docker: seatsurfing-db-1&#124;postgres:16&#124;Up 2w&#124;5432/tcp |
| 54 | E-047 | Docker: countdown-demo.web.1&#124;dokku/countdown-demo:latest&#124;Up 2w&#124;5000/tcp |
| 55 | E-048 | Docker: authentik-server-1&#124;ghcr.io/goauthentik/server:2026.5.0&#124;Up healthy&#124;7080-&gt;9000,7443-&gt;9443 |
| 56 | E-049 | Docker: authentik-worker-1&#124;ghcr.io/goauthentik/server:2026.5.0&#124;Up healthy&#124;no ports |
| 57 | E-050 | Docker: authentik-redis-1&#124;redis:alpine&#124;Up healthy&#124;6379/tcp |
| 58 | E-051 | Docker: authentik-postgresql-1&#124;postgres:12-alpine&#124;Up healthy&#124;no ports |
| 59 | E-052 | Docker: authentik-postgresql_16-1&#124;postgres:16-alpine&#124;Up healthy&#124;5432/tcp |
| 60 | E-053 | Docker: dockhand-dockhand-1&#124;fnsys/dockhand:latest&#124;Up healthy&#124;9443-&gt;3000 |
| 61 | E-054 | Docker: dockhand-postgres-1&#124;87e04d274d18&#124;Up 2w&#124;5432/tcp |
| 62 | E-055 | Docker: dokku&#124;dokku/dokku:0.37.6&#124;Up 2w&#124;3022-&gt;22,4080-&gt;80,4443-&gt;443 |
| 63 | E-056 | Docker: statping&#124;adamboutcher/statping-ng&#124;Up healthy&#124;5080-&gt;8080 |
| 64 | E-057 | Docker: node-exporter&#124;prom/node-exporter:latest&#124;Up 2w&#124;9100-&gt;9100 |
| 65 | E-058 | Docker: portainer_agent&#124;7694bd834ce7&#124;Up 2w&#124;9001-&gt;9001 |
| 66 | E-059 | Docker: dokku.mongo.wealth-day-db&#124;mongo:8.0.13&#124;Up 2w&#124;27017/tcp |
| 67 | E-060 | Docker: dokku.mongo.edm-generator-db&#124;mongo:8.0.13&#124;Up 2w&#124;27017/tcp |
| 68 | E-061 | Docker: seatsurfing-admin-ui-1&#124;4b70b5b2af35&#124;Up 2w&#124;3000/tcp |
| 69 | E-062 | Docker: seatsurfing-booking-ui-1&#124;4105231eaa91&#124;Up 2w&#124;3001/tcp |
| 70 | E-063 | Docker: raise-storybook.web.1&#124;dokku/raise-storybook:latest&#124;Up 2w&#124;none |
| 71 | E-064 | Docker: download-pdfs-from-url.web.1&#124;dokku/download-pdfs-from-url:latest&#124;Up 2w&#124;none |
| 72 | E-065 | Docker: dokku.mongo.ocbc-moa-prototype&#124;mongo:8.0.13&#124;Up 2w&#124;27017/tcp |
| 73 | E-066 | Docker: section-website-prod.web.1&#124;dokku/section-website-prod:latest&#124;Up 2w&#124;3000/tcp |
| 74 | E-067 | Docker: section-website-staging.web.1&#124;dokku/section-website-staging:latest&#124;Up 2w&#124;3000/tcp |
| 75 | E-068 | Docker: section-dashboard.web.1&#124;dokku/section-dashboard:latest&#124;Up 2w&#124;3001/tcp |
| 76 | E-069 | Docker: ocbc-eco-api.web.1&#124;dokku/ocbc-eco-api:latest&#124;Up 2w&#124;none |
| 77 | E-070 | Docker: section-namecard-api.web.1&#124;dokku/section-namecard-api:latest&#124;Up 2w&#124;3000/tcp |
| 78 | E-071 | Docker: section-hello.web.1&#124;dokku/section-hello:latest&#124;Up 2w&#124;3000/tcp |
| 79 | E-072 | Docker: ocbc-oa-vendor-api.web.1&#124;dokku/ocbc-oa-vendor-api:latest&#124;Up 2w&#124;none |
| 80 | E-073 | Docker: ocbc-mb-life-goals-mock-api.web.1&#124;dokku/ocbc-mb-life-goals-mock-api:latest&#124;Up 2w&#124;none |
| 81 | E-074 | Docker: resource-soketi&#124;quay.io/soketi/soketi:1.4-16-debian&#124;Up 2w&#124;6002-&gt;6001,9602-&gt;9601 |
| 82 | E-075 | Docker: order-soketi&#124;quay.io/soketi/soketi:1.4-16-debian&#124;Up 2w&#124;6001-&gt;6001,9601-&gt;9601 |
| 83 | E-076 | Shallow dirs: /var/www/html; /home app dirs; four .old: gcmd-ext2, bc-ext2, smu-blog-ext2, smu-staging-ext2. |
| 84 | E-077 | Nginx auth1.wearesection.com.conf: auth1.wearesection.com; root /home/wearesection-auth1/...; proxy_pass 6443,5443. |
| 85 | E-078 | Nginx auth.ripplewerkz.co.conf: auth.ripplewerkz.co; root /home/ripplewerkz-auth/...; proxy_pass 7080. |
| 86 | E-079 | Nginx auth.wearesection.com.conf: auth.wearesection.com; root /home/wearesection-auth/...; proxy_pass https://127.0.0.1:7443. |
| 87 | E-080 | Nginx bc.ext2.wearesection.com.conf: bc.ext2.wearesection.com; root .../public; proxy_pass 8080. |
| 88 | E-081 | Nginx beta-v1.wearesection.com.conf: beta-v1.wearesection.com; root /home/wearesection-beta-v1/...; proxy_pass 4080. |
| 89 | E-082 | Nginx browserless.dokku.wearesection.com.conf: browserless.dokku.wearesection.com; proxy_pass 6000. |
| 90 | E-083 | Nginx cfssff.com.conf: www.cfssff.com/cfssff.com/www1.cfssff.com; proxy_pass 4080. |
| 91 | E-084 | Nginx countdown-demo.dokku.wearesection.com.conf: countdown-demo.dokku.wearesection.com; proxy_pass 4080. |
| 92 | E-085 | Nginx custom-domain.conf: panel1.wearesection.com; root /home/clp/htdocs/app/files/public; proxy_pass https://127.0.0.1:8443/. |
| 93 | E-086 | Nginx default.conf: server_name _; listen 80/443 default_server. |
| 94 | E-087 | Nginx docker.cms.wearesection.com.conf: docker.cms.wearesection.com; proxy_pass 9443. |
| 95 | E-088 | Nginx dokku.wearesection.com.conf: dokku.wearesection.com; proxy_pass https://127.0.0.1:4443. |
| 96 | E-089 | Nginx download-pdfs-from-url.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 97 | E-090 | Nginx dozz.ripplewerkz.co.conf: dozz.ripplewerkz.co; proxy_pass 8090. |
| 98 | E-091 | Nginx edm-generator.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 99 | E-092 | Nginx gcmd.ext2.wearesection.com.conf: gcmd.ext2.wearesection.com; root ...; proxy_pass 8080. |
| 100 | E-093 | Nginx hhmw.ext2.wearesection.com.conf: hhmw.ext2.wearesection.com; root /home/wearesection-hhmw-ext2/... |
| 101 | E-094 | Nginx hotdesk.gravitas.my.conf: hotdesk.gravitas.my; proxy_pass 7070. |
| 102 | E-095 | Nginx hotdesk.wearesection.com.conf: hotdesk.wearesection.com; proxy_pass 7070. |
| 103 | E-096 | Nginx inventory.wearesection.com.conf: inventory.wearesection.com; root .../public. |
| 104 | E-097 | Nginx keppel-plot6.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 105 | E-098 | Nginx my.wiki.wearesection.com.conf: my.wiki.wearesection.com; proxy_pass 5000. |
| 106 | E-099 | Nginx ocbc-csl-api.dokku.wearesection.com.conf: domain same; proxy_pass https://127.0.0.1:4443. |
| 107 | E-100 | Nginx ocbc-eco-api.dokku.wearesection.com.conf: domain same; proxy_pass https://127.0.0.1:4443. |
| 108 | E-101 | Nginx openapi-hs-cussec.wearesection.com.conf: domain same; proxy_pass 1081. |
| 109 | E-102 | Nginx openapi-hs-form.wearesection.com.conf: domain same; proxy_pass 1080. |
| 110 | E-103 | Nginx order.wearesection.com.conf: order.wearesection.com; root .../public; proxy_pass 6001,8080. |
| 111 | E-104 | Nginx prototype-one.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 112 | E-105 | Nginx prototype-two.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 113 | E-106 | Nginx pru-fa.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 114 | E-107 | Nginx raise-storybook.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 115 | E-108 | Nginx resource.wearesection.com.conf: resource.wearesection.com; root .../public; proxy_pass 8080,6002. |
| 116 | E-109 | Nginx sccb.ext2.wearesection.com.conf: sccb.ext2.wearesection.com; root /home/wearesection-sccb-ext2/... |
| 117 | E-110 | Nginx section-dashboard.dokku.wearesection.com.conf: server_name section-dashboard; proxy_pass 4080, 4080/verify, 4080/profile. |
| 118 | E-111 | Nginx section-hello.dokku.wearesection.com.conf: server_name section-hello; proxy_pass 4080, 4080/verify, 4080/profile. |
| 119 | E-112 | Nginx section-namecard-api.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 120 | E-113 | Nginx section-website-prod.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 121 | E-114 | Nginx smu-blog.ext2.wearesection.com.conf: wildcard + smu-blog.ext2.wearesection.com; root .../web. |
| 122 | E-115 | Nginx smu-staging.ext2.wearesection.com.conf: smu-staging.ext2.wearesection.com; root .../web. |
| 123 | E-116 | Nginx sph.ext2.wearesection.com.conf: sph.ext2.wearesection.com; root /home/wearesection-sph-ext2/... |
| 124 | E-117 | Nginx uptime.ripplewerkz.co.conf: uptime.ripplewerkz.co; proxy_pass 5080. |
| 125 | E-118 | Nginx utcors-proxy.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 126 | E-119 | Nginx wealth-day.dokku.wearesection.com.conf: domain same; proxy_pass 4080. |
| 127 | E-120 | Nginx wiki.gravitas.my.conf: wiki.gravitas.my; proxy_pass 5001. |

## Review Steps

| Row | A | B | C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Review order and next steps |  |  |  |  |  |  |  |
| 4 | Step ID | Order | Stage | Action | Responsible role | Prerequisite | Expected result | Current status |
| 5 | STEP-01 | 1 | Inspect this VM | Record workloads, routes and host details. | Reviewer | Read-only SSH access | Inventory and audit notes recorded. | Completed for this VM |
| 6 | STEP-02 | 2 | Identify each owner | Use 03 Owner Review to assign an actual owner to each item. | Reviewer / project leads | VM inventory | Each row has a named owner or a recorded escalation. | Not started |
| 7 | STEP-03 | 3 | Ask each owner | Ask whether the item is still used, why it exists, and what depends on it. | Reviewer + item owner | Owner identified | Written response and evidence captured for each item. | Not started |
| 8 | STEP-04 | 4 | Propose retain or retire | Compare owner responses with dependencies, usage and retention needs. | Reviewer + technical owner | Owner response and technical evidence | An item-specific proposal with rationale; no deletion yet. | Not started |
| 9 | STEP-05 | 5 | Organize retained items | Propose project, environment, owner, repository and naming for retained items. | Technical owner / DevOps | Purpose and ownership confirmed | A clear ownership and deployment structure. | Not started |
| 10 | STEP-06 | 6 | Prepare any cleanup | Document exact scope, backup, restore check, rollback and maintenance window. | DevOps | A reviewed retain/retire proposal | A concrete change plan for approval. | Not started |
| 11 | STEP-07 | 7 | Execute approved changes | Only carry out the explicitly approved changes and verify affected services. | DevOps | Separate change approval | Change log, service verification and updated inventory. | Not started |
| 12 | STEP-08 | 8 | Extend beyond this VM | Review the remaining DigitalOcean resources and company DNS records. | Reviewer + DO / DNS owners | Read access to the relevant control planes | Separate account-wide and DNS inventories. | Not started |

