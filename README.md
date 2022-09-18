# keycloak_ha
keycloak_ha

1-) docker-compose --env-file ./keycloak.env --file ./docker-compose-haproxy-ispn-remote.yml up

	https://id.acme.test:1443/auth

2-) docker-compose --env-file ./keycloak.env --file ./docker-compose-haproxy-ispn-izmir-remote.yml up

	https://id.izmir.acme.test:1444/auth


-----------------------------
connect brige to containers
-----------------------------
docker network connect app_net keycloak_ha_acme-keycloak-db-izmir_1