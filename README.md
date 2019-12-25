Docker compose
: tool for defining & running multi-container docker applications
: use yaml files to configure application services (docker-compose.yml)
: can start all services with a single command : docker compose up
: can stop all services with a single command : docker compose down
: can scale up selected services when required

Step 1 : install docker compose
   (already installed on windows and mac with docker)
   docker-compose -v
   
   2 Ways

   1.  https://github.com/docker/compose/releases

   2. Using PIP
    pip install -U docker-compose
    
    There can be some problems while checking the version of docker-compose due to broken pip.
    In order to fix the issue ending "AttributeError: 'module' object has no attribute 'SSL_ST_INIT' " 
    , run the following commands:
         rm -rf /usr/lib/python2.7/dist-packages/OpenSSL
         rm -rf /usr/lib/python2.7/dist-packages/pyOpenSSL-0.15.1.egg-info
         sudo pip install pyopenssl
     After running this, check the version of docker-compose .

Step 2 : Create docker compose file at any location on your system
   docker-compose.yml

Step 3 : Check the validity of file by command
    docker-compose config

Step 4 : Run docker-compose.yml file by command
   docker-compose up -d

Steps 5 : Bring down application by command
   docker-compose down

TIPS
How to scale services( here I have scaled database as a service)

—scale
docker-compose up -d --scale database=4
