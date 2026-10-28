PRESYO-KUWENTA: OFFLINE + ONLINE VERSION

MGA FILE
- index.html: pangunahing web app
- sw.js: offline cache (Service Worker)
- manifest.webmanifest: installable web app metadata
- Code.gs: backend para magsave sa Google Sheets

PAANO GUMAGANA
1. Kailangang i-host ang index.html, sw.js at manifest.webmanifest sa iisang HTTPS website (hal. GitHub Pages). Ang Service Worker ay hindi gagana sa lahat ng sitwasyon kung bubuksan lang ang HTML bilang file://.
2. Unang beses buksan ang website habang may internet; pagkatapos ma-cache ang app, puwede itong gamitin offline sa parehong browser/device.
3. Offline, kapag pinindot ang “Kuwentahin ang PED”, awtomatikong mase-save ang result sa IndexedDB ng device.
4. Online syncing: gumawa ng Google Sheet. Kopyahin ang ID sa URL sa pagitan ng /d/ at /edit.
5. Sa https://script.google.com/ gumawa ng bagong project, palitan ang Code.gs ng laman ng kasamang Code.gs, at ilagay ang Spreadsheet ID sa SPREADSHEET_ID.
6. Deploy > New deployment > Web app. Execute as: Me. Access: piliin ang naaayon sa school policy; para sa simpleng public classroom test, maaaring “Anyone” kung pinapayagan ng inyong account/patakaran. I-authorize at kopyahin ang URL na nagtatapos sa /exec.
7. Sa app, ilagay ang Web App URL sa field na “Google Apps Script Web App URL” at pindutin ang “I-save ang sync settings”.
8. Kapag online, subukan ang “I-sync ngayon”. Ang mga resultang may kumpirmasyon ay mamarkahang synced. Gumagamit ang backend ng unique Record ID para maiwasan ang duplicate kapag naulit ang pagpapadala.

MAHALAGANG LIMITASYON / PRIVACY
- Ang local records ay nakaimbak sa browser/device; hindi ito awtomatikong lumilipat sa ibang device. Huwag i-clear ang browser data bago ma-sync ang pending results.
- Kailangang online at naka-open ang app (o bumalik sa app) para tumakbo ang sync.
- Gumamit ng learner code sa halip na buong pangalan. Iwasang magtala ng sensitibong personal data.
- Ang access sa Google Sheet at web app ay dapat sundin ang school privacy rules.
- Ito ay prototype. Bago gamitin sa aktuwal na action research, subukan muna sa dummy data at tiyaking tama ang permissions at sheet records.
