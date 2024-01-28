### Commands that led to a running .NET 7 web API in Docker container and serving it at localhost:5001/weatherforecast:
```
 1188  git clone https://github.com/eubanks-dev/simple-dotnet-core-api-with-aws-ecs-fargate-using-terraform.git
 1189  ls
 1190  cd simple-dotnet-core-api-with-aws-ecs-fargate-using-terraform
 1191  vi Makefile
 1192  vi Dockerfile
 1193  bat Dockerfile
 1194  make lab
 1195  docker
 1196  make lab
 1197  yum search dotnet-sdk
 1198  yum
 1199  vi Dockerfile
 1200  bat Dockerfile
 1201  make lab
 1202  vi Dockerfile
 1203  make lab
 1204  vi Dockerfile
 1205  make lab

(I think I did the below to temporarily enable logging)
 1206  export DOCKER_BUILDKIT=0
 1207  make lab
 1208  export DOCKER_BUILDKIT=


 1209  vi Dockerfile
 1210  make lab
 1211  vi Dockerfile
 1212  ls
 1213  make login-lab

Switched to MS tutorial: https://learn.microsoft.com/en-us/dotnet/core/docker/build-container?tabs=linux&pivots=dotnet-8-0
 1214  dotnet
 1215  dotnet --info
 1216  dotnet new console -o App -n DotNet.Docker
 1217  ls
 1218  cd App
 1219  ls
 1220  tree
 1221  dotnet run
 1222  cd ..
 1223  ls
 1224  rm -rf App
 1225  vi Dockerfile
 1226  bat Makefile
 1227  dotnet new webapi -o webapi --no-https
 1228  ls
 1229  dotnet run -p webapi --urls=http://*:5000/
 1230  ls
 1231  dotnet run -p webapi --urls='http://*:5000/'
 1232  dotnet run -p webapi --urls=http://localhost:5000/
 1233  vi webapi/Controllers/WeatherForecastController.cs
 1234  dotnet run -p webapi --urls=http://localhost:5000/
 1235  bat webapi/Controllers/WeatherForecastController.cs
 1236  bat webapi/Program.cs
 1237  bat webapi/WeatherForecast.cs
 1238  dotnet run -p webapi --urls=http://localhost:5000/
 1239  dotnet run -p webapi
 1240  cd webapi
 1241  ls
 1242  vi appsettings.json
 1243  vi Controllers/WeatherForecastController.cs
 1244  dotnet run
 1245  ls
 1246  cd ..
 1247  ls
 1248  history | grep dotnet
 1249  cd webapi
 1250  code .
 1251  bat ~/.profile
 1252  bat ~/.zprofile
 1253  bat ~/.zshrc
 1254  grep "PATH=" ~/
 1255  grep "PATH=" ~/*
 1256  grep -r -I -D skip "PATH=" ~/*
 1257  grep -I -D skip "PATH=" ~/*
 1258  man grep
 1259  grep "PATH=" ~/.*
 1260  code .
 1261  dotnet publish -c Release
 1262  ls bin/Release/net7.0/publish
 1263  ls
 1264  bat ../Dockerfile
 1265  vi Dockerfile
 1266  dotnet --info
 1267  vi Dockerfile
 1268  bat Dockerfile
 1269  ls -lrt
 1270  docker build -t counter-image -f Dockerfile .
 1271  docker images
 1272  vi Dockerfile
 1273  grep -r "counter-image" .
 1274  docker build -t webapi-image -f Dockerfile .
 1275  docker images
 1276  bat Dockerfile
 1277  docker create --name webapi-container webapi-image
 1278  docker ps -a
 1279  docker start webapi-container
 1280  docker ps
 1281  docker ps -a
 1282  docker start 32839718be14
 1283  docker ps
 1284  docker ps -a
 1285  docker start webapi-container
 1286  bat Dockerfile
 1287  docker run -d -p 5001:80 webapi-image
 1288  docker ps
 1289  docker logs
 1290  docker logs webapi-container
 1291  find . -name *.dll
 1292  ls bin/Release/net7.0/publish
 1293  vi Dockerfile
 1294  history | grep docker
 1295  docker build -t webapi-image -f Dockerfile .
 1296  docker images
 1297  docker create --name webapi-container webapi-image
 1298  docker rm webapi-container
 1299  docker create --name webapi-container webapi-image
 1300  docker start webapi-container
 1301  docker ps
 1302  docker stop webapi-container
 1303  docker ps
 1304  docker run -d -p 5001:80 webapi-image
 1305  docker ps
 1306  docker stop webapi-container
 1307  docker stop gracious_hawking
 1308  docker start webapi-container
 1309  docker ps
 1310  docker stop webapi-container
 1311  docker ps
 1312  docker start -d -p 5001:80 webapi-image
 1313  docker ps
 1314  docker run -d -p 5001:80 webapi-image
```
