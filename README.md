# synology-docker

komodo templates for my docker compose files
- .env files locally on machine and backed up with hyperbackup 
- location.env file because it's annoying to constantly specify timezone :) 

## handy commands
for updates (if not using komodo): 
`docker-compose down && docker-compose pull && docker-compose up -d` 

for pruning:
`docker image prune -f && docker volume prune -f && docker network prune -f`

## notes
- PMS needs to run in `network_mode: host` for local network discovery

other, pretty irrelevant notes:
- for tailscale purposes: https://forums.plex.tv/t/ability-to-manually-set-public-ip-for-remote-access/189111/24?utm_source=pocket_mylist
- certs were created with acme https://github.com/acmesh-official/acme.sh/wiki/Synology-NAS-Guide 

## other stuff
recursive hard linking: 
`cp -lR /original /other`

checking inode #
`ls -i` 

replace NUM with inode# to check other nodes
`find . -inum NUM`
