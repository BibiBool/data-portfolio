COMPOSE_FILE := docker-compose.yaml

perms:
	sudo mkdir -p logs plugins dags raw_data clean_data consolidated_data emr-scripts notebooks && sudo chmod -R u=rwx,g=rwx,o=rwx logs plugins dags raw_data clean_data consolidated_data emr-scripts notebooks

docker-spin-up:
	docker compose up airflow-init && docker compose up

up:	perms docker-spin-up

down:
	docker compose down

clean: down
	docker compose down

.PHONY: up down clean