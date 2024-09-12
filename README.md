# clio-ai
ClioAI is an AI-powered platform that provides answers based on classical sources from Ancient Greece and Rome. Using a Retrieval-Augmented Generation (RAG) model, it references texts from authors like Homer, Plato, and Cicero, delivering accurate explanations along with citations from the original works for a rich, educational experience.

## Elastic

docker volume create esdata

docker run -it --rm --name elasticsearch -m 4GB -p 9200:9200 -p 9300:9300 -v esdata:/usr/share/elasticsearch/data -e "discovery.type=single-node" -e "xpack.security.enabled=false" -e "ES_JAVA_OPTS=-Xms1g -Xmx1g" docker.elastic.co/elasticsearch/elasticsearch:8.15.0

Check count of indexed data: curl -X GET "http://localhost:9200/ancient_sources_db_index/_count"