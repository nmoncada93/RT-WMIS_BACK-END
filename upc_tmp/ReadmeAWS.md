# AWS

`sudo lsof -i`

`sudo kill -9 <PID>` Detiene procesos


Reconectar maquina AWS:

ssh -i C:\clavesAWS/uoc.edu17307e9f3d7d9f75d998a2891bb4d00a808ae83c.pem ubuntu@3.254.186.70 -p 55000


Actualizar app.py:

`scp -P 55000 -i C:\clavesAWS\uoc.edu17307e9f3d7d9f75d998a2891bb4d00a808ae83c.pem C:\clavesAWS\backend\app.py ubuntu@3.254.186.70:/home/ubuntu/backend/`

`scp -P 55000 -i C:\clavesAWS\uoc.edu17307e9f3d7d9f75d998a2891bb4d00a808ae83c.pem C:\clavesAWS\backend\networkstations.json ubuntu@3.254.186.70:/home/ubuntu/backend/static/`

ssh -i C:\clavesAWS\uoc.edu17307e9f3d7d9f75d998a2891bb4d00a808ae83c.pem ubuntu@3.254.186.70 -p 55000


`cd ~/backend`

`ls -la`

`source venv/bin/activate`


`pkill gunicorn`


gunicorn -w 4 -b 0.0.0.0:55001 app:app


sudo lsof -i :55001


curl http://127.0.0.1:55001/api/network-stations


curl -k https://34.245.163.23/api/network-stations

