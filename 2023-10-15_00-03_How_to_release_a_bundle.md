1. `git checkout main`
2. `git merge development`
3. Odpalić aplikację lokalnie yarn build && yarn start, przeklikać i upewnić się że zmiany działają. Jak coś nie działa to naprawić jak się da.
4. `yarn changelog`
5. Wstawić wyniki do CHANGELOG.md pod nową wersją (patch jak bugfixy, minor jak ficzery, major jak jest niekompatybilne wstecznie). Poformatować by nie było merge commitów i powstawiać numery ticketów jak się da.
6. `git commit -m "chore: changelog for x.y.z"`
7. `git tag x.y.z`
8. `git push && git push --no-verify --tags`
9. Wejść na pipelines, jak build dla taga przejdzie to kliknąć play na Pilot, odczekać minutkę i kliknąć play na Preview.
Prześledzić deployment na argo (pilot i preview wejdą w stan “progressing” po paru minutach, a po paru następnych powinny być znowu “healthy”)
na preview w konsoli sprawdzić `$('meta[name=version]').getAttribute('content')` — jak jest nowy to kolejny pkt
10. Zaanonsować bundle na #release jak np tu
11. `git checkout development`
12. `git merge main i git pushngelog`