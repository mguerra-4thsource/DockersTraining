# dockertest
dockerTest

Commands:

cls
docker --version
docker ps
docker ps -a
docker images
create --name baseproject dockerstrainingcomposemiguelguerra:dev -p 80 
docker build -f "C:\Users\miguel.guerra\source\repos\DockersTraining_Compose_miguel_guerra\DockersTraining_Compose_miguel_guerra\Dockerfile" --force-rm -t dockerstrainingcomposemiguelguerra:dev --target base  --label "com.microsoft.created-by=visual-studio" --label "com.microsoft.visual-studio.project-name=DockersTraining_Compose_miguel_guerra" "C:\Users\miguel.guerra\source\repos\DockersTraining_Compose_miguel_guerra" 
docker create --name site1 dockerstrainingcomposemiguelguerra:dev -p 8085 -e "AppSettings:storename"="site1"
docker create --name site2 dockerstrainingcomposemiguelguerra:dev -p 8086 -e "AppSettings:storename"="plano"
docker tag 0109bb110ba3 mguerra4th/dockers-training:dockerTest
docker push mguerra4th/dockers-training:dockerTest
