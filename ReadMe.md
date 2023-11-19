# Vorraussetzungen

* Python3 (>3.9) [[1]](#1)
* Ansible [[2]](#2)
  * ggf. zur PATH-Variable hinzufügen; Konsolen output beachten

# Server einrichten

## Keycloak
* Admin Username und Passwort verändern! - siehe Keycloak ToDos

## Allgemein
* IPs der Hosts in der "hosts"-Datei anpassen
* Ansible auf dem Server ausführen
  * `ansible-playbook -i hosts playbook.yml`

#  Nutzung

## Keycloak
* Erreichbar unter: https://luminaa.chat:8080/admin/master/console/


# ToDos

## Allgemein
- [ ] Eigene Role für das vorbereiten des Servers zB.: `apt -y update` und `apt -y upgrade`
  -  Wird aktuell in der keycloak-db ausgeführt
- [ ]  Doku für nginx 
- [ ]  Doku für mongoDB

## Keycloak (+DB)
- [x] ~~Keycloak mit Postgres verbinden~~
- [ ] Hart codierte Werte mit Variablen ersetzten
  - [ ] keycloak.conf
  - [ ] keycloak.service 
  - [ ] main.yml
  - [ ] keycloak-db/main.yml
- [ ] `start-dev` mit `start` Command ersetzten
- [ ] Richtigen command für systemctlm Befehle verwenden
- [ ] Mehr bedingte Ausführungen hinzufügen in der main.yml (zB. JDK nur installieren falls noch nicht vorhanden)


## Ressourcen
<a id="1">[1]</a> 
https://www.python.org/downloads
<br>
<a id="2">[2]</a> 
https://docs.ansible.com/ansible/latest/getting_started/get_started_ansible.html
