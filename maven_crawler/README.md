# maven-crawler
This repo contains code for crawling the Maven repos and extracting metadata about projects.
The metadata is gathered from POM files.


## Docker
Build the Docker image:
```
docker build -t maven_crawler .
```

To start the crawler on the Linux server, run the following command:

```
docker run --network="host" maven_crawler --m "https://repo1.maven.org/maven2/" --p "./maven2" --q q_items.txt --c 0.3 --h localhost:30001
```
