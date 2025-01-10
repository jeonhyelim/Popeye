# POPEYE project(DEVOPS)
<br/><br>
The application is composed of 5 elements:
- Poll, a Flask Python web application that gathers votes and push them into a Redis queue.
- A Redis queue, which holds the votes sent by the Poll application, awaiting for them to be consumed by the Worker.
- The Worker, a Java application which consumes the votes being in the Redis queue, and stores them into a PostgreSQL database.
- A PostgreSQL database, which (persistently) stores the votes stored by the Worker.
- Result, a Node.js web application that fetches the votes from the database and displays the. . . well, result. ;)
 <br/><br>


Getting start with:
```sh
docker-compose up --build
```
<br/><br>
The result:  

seeing Poll on localhost:5000/ and Result on localhost:5001/  



<img width="1440" alt="스크린샷 2024-03-06 오후 3 26 41" src="https://github.com/EpitechPromo2028/B-DOP-200-PAR-2-1-popeye-hyelim.jeon/assets/114721039/539c338b-1340-4a1f-8342-b9e73ee6367d">
