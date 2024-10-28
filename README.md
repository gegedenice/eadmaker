# eadmaker
A Python Flask app to manage EAD/XML files (create, update...) with AI assistants

## Status

In progress...

## Install with Docker

A Docker image of the app is available in Docker hub : 

```
docker pull smartbiblia/eadmaker:latest
```
To run the container : 

```
docker run -d --name eadmaker \
  -e HUGGINGFACE_TOKEN=<your_huggingface_token> \
  -e GROQ_API_KEY=<your_groq_api_key> \
  -p 5000:5000 \
  -v <your_path>:/app/static/xml_files \ # ead/xml files
  -v <your_path>:/app/static/rico_outputs \ # ead/xml files converted in RiCo
   smartbiblia/eadmaker:latest
```

