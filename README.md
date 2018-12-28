#### CS293D HW1 Part 1
Henry Yu, Krassimir Djonev

##### Directions to run:
1. Download and install solr-7.2.1
2. (While inside the solr-7.2.1 directory) run “bin/solr start” to start up a Solr Instance
3. Check  http://localhost:8983 to see that it has successfully launched
4. Create a core named “trec45” so that we can upload data to Solr by running “bin/solr create_core -c trec45”
5. (While inside the directory of my code repository) run “mvn clean compile” and then “mvn package”
6. Upload the “trecSmall.xml” file to the launched Solr instance by running  “java -cp target/cs293dhw1-1.0-SNAPSHOT-jar-with-dependencies.jar cs293d_hw1.DocumentUploader -docs trecSmall.xml”
7. Check that the dataset has been successfully uploaded by checking at http://localhost:8983/solr/trec45/browse
8. Index the dataset uploaded on Solr by running  “java -cp target/cs293dhw1-1.0-SNAPSHOT-jar-with-dependencies.jar cs293d_hw1.DocumentIndexer -docs trecSmall.xml”
9. We can now start the web service to query the dataset by running “java -jar target/cs293dhw1-1.0-SNAPSHOT-jar-with-dependencies.jar”
10. Check http://localhost:4567/ to use the web service