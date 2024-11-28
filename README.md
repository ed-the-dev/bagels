command shift v to open preview window for this as I always forget.

#### Front End

`docker build -t bagels-front-end ./front-end`

`docker run -it -p 8080:8080 -v $(pwd)/front-end:/code bagels-front-end bash`


#### Open Trip Planner

Street network https://download.geofabrik.de/europe/united-kingdom/england/greater-london.html

TODO: make a note of where we get our data from

`docker build -t open-trip-planner ./open-trip-planner`

Run container command

`docker run -it -p 8080:8080 -v $(pwd)/open-trip-planner:/code open-trip-planner bash`

from within code directory of container:

Build Graph:

`java -Xmx24G -jar otp-2.6.0-shaded.jar --build --save .`

Load graph and serve

`java -Xmx24G -jar otp-2.6.0-shaded.jar --load .`

server url: http://localhost:8080/graphiql

#### Back-End

https://actix.rs/docs/websockets

#### Front End
 
Flutter