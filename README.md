FRONTEND-
cd frontend
npm install
npm run dev

BACKEND-
mvn spring-boot:run

MAKE SURE MYSQL IS OPEN AND turotdb IS RUNNING

DOCKER-
docker compose build

docker tag cicd-portfolio-backend:latest ramcharan0101/cicd-portfolio-backend:latest

docker tag cicd-portfolio-frontend:latest ramcharan0101/cicd-portfolio-frontend:latest


docker login


docker push ramcharan0101/cicd-portfolio-backend:latest

docker push ramcharan0101/cicd-portfolio-frontend:latest


kubectl apply -f k8s/backend-deployment.yaml

kubectl apply -f k8s/frontend-deployment.yaml

kubectl apply -f k8s/ingress.yaml


kubectl get svc

kubectl get ingress
