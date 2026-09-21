# LB 324

## Aufgabe 2

Erklären Sie hier, wie man `pre-commit` installiert.

Zuerst müssen die benötigten Python-Abhängigkeiten installiert werden. Dazu wird im Projektordner folgender Befehl ausgeführt:

pip install -r requirements.txt

Anschliessend werden die pre-commit Hooks für commit und push installiert:

pre-commit install --hook-type pre-commit --hook-type pre-push

Damit wird automatisch bei jedem git commit Black ausgeführt und der Code formatiert. Bei jedem git push werden die Tests mit pytest ausgeführt. Wenn die Tests fehlschlagen, wird der Push verhindert.

Zum Überprüfen und erstmaligen Ausführen der Hooks kann man anschliessend folgenden Befehl verwenden:

pre-commit run --all-files

## Aufgabe 4

Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.

Die Applikation läuft unter: https://kohanovmaxim-lb324-e0hzhhcbdsfcd4g9.germanywestcentral-01.azurewebsites.net/
Password: MaximKohanov

Passwort auf Azure setzen:
Man geht auf Azure Portal -> App Services -> Web App öffnen
Danach auf Settings -> Environment variables -> App settings -> Add
Man setzt den Namen gleich "PASSWORD", Wert = GitHub Benutzername
Danach auf Apply + Confirm klicken und App neu starten
