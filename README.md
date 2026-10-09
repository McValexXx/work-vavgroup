# Work VAVGROUP

Dashboard comparativ în limba rusă pentru ФОРМА ДЛЯ ОХРАНЫ.

Site: https://work.vavgroup.pro

Publicarea automată folosește Cloudflare Pages, proiectul `work-vavgroup`, conectat la ramura `main` din acest repository. Modificările salvate în `main` declanșează publicarea. Starea fiecărei publicări se vede în Cloudflare → Workers & Pages → work-vavgroup → Deployments.

Setări: framework `None`, rădăcină repository, director publicat `dist`. Comanda de construire:

```sh
mkdir -p dist && cp index.html dist/ && if [ -d dashboards ]; then cp -R dashboards dist/; fi
```

Comanda publică pagina principală și directorul `dashboards`, inclusiv fișierele paginilor din acesta. Documentația și ofertele originale nu sunt copiate în site. Adresa de rezervă: https://work-vavgroup.pages.dev.

Pagina este autonomă: HTML, stiluri și calculator local, fără biblioteci externe. Ofertele și diferențele de TVA sunt documentate în dashboard. Nu există prognoze sau garanții de rezultate.

## Dashboard-uri viitoare

1. Pregătiți o pagină HTML autonomă, adaptată pentru iPhone, cu datele și sursele verificate.
2. Puneți pagina în `dashboards/nume-dashboard/index.html`. Folosiți un nume unic, cu litere latine, cifre și cratime.
3. Încărcați fișierele în repository și salvați modificarea în `main`.
4. După publicarea automată, pagina este disponibilă la `https://work.vavgroup.pro/dashboards/nume-dashboard/`.
5. Verificați linkul și calculatorul pe iPhone. Accesul fără VPN se verifică în rețeaua destinatarului.

Pentru actualizarea dashboard-ului actual, modificați `index.html`. Domeniul VAVGROUP principal nu are nevoie de modificări pentru fiecare dashboard.

În interfața GitHub: `Add file` → `Upload files` → selectați pagina și fișierele ei → `Commit changes` în `main`. Pentru o pagină nouă, păstrați structura `dashboards/nume-dashboard/` la încărcare. Cloudflare gestionează domeniul separat; fișierul GitHub Pages `CNAME` nu este necesar.

Încărcarea publică o pagină deja pregătită; nu transformă automat ofertele PDF în dashboard. Un repository privat nu garantează că site-ul publicat este privat. Nu publicați parole, date personale sau materiale confidențiale fără acord.

După aprobarea directorului, dashboard-ul temporar poate fi retras separat; istoricul Git păstrează versiunile anterioare.
