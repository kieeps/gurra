# Exempel
Har gjort en composefil med 2 "services" i.

Det som behöver göras är att ändra /path/to/folder/on/server/ så det blir till en riktig mapp på servern.
Om detta är en LXC (det skulle jag rekomendera) så kan man göra så att te.x /lagring/docker i LXC instansen går till /lagring/docker på proxmox servern.

Kopiera docker-compose.yml filen till din home mapp på LXC servern och kör ```docker-compose pull``` för att ladda hem alla den senaste "container imagen" per service
Kör sedan ```docker-compose up -d``` för att starta alla services i den composefilen

# Bra commands

- docker-compose up -d
   - startar alla services

- docker-compose pull
   - dra hem alla de senaste images

- docker logs <service>
   - visar loggarna för specifik service

- docker system prune
    - rensar bort alla oanvända images/nätverk/volymer för docker

- docker-compose stop <service>
    - stoppar specifik services i composefilen

- docker-compose down
    - stoppar och tar bort alla services från systemet

- docker-compose restart <service>
    - startar om specifik service i composefilen