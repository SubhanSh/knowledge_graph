before cloning the project you need to install ollama:
```bash
docker pull ollama/ollama

docker run --rm -d --name ollama \
  -p 11434:11434 \
  -v ollama_data:/root/.ollama \
  ollama/ollama

docker exec -it ollama ollama pull zephyr

docker run --rm -d --name ollama \
  -p 11434:11434 \
  -v ollama_data:/root/.ollama \
  ollama/ollama serve
```

if you want to chat with ollama:
```bash
docker exec -it ollama ollama run zephyr
```

```bash
git clone https://github.com/rahulnyk/knowledge_graph.git
cd knowledge_graph

poetry install
```

If package aiohttp has error in installation then run
```bash
poetry update aiohttp
```

installing notebook(jupyter notebook):
```bash
poetry add notebook --group dev
```

then run jupyter:
```bash
poetry run jupyter lab
```


now in jupyter from "run" menu click on "Run all cells" to run the code.

it read the document text from /data_input/cureus/any-name.txt.

the the knowledge graph will be written in /docs/index.html file.
