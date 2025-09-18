## Instructions to build a Container Image 

  * Base Image : `python:3.9-slim`
  * Copy over everything in the build context (streamlit_app) path
  * Installing Dependencies : `pip install -r requirements.txt`
  * Port: 8501 
  * Launch Command : `streamlit run app.py --server.address=0.0.0.0`

1. Create my Docker image
```bash
docker image build -t streamlit .
```

2. Launch my image
```bash
docker run -idtP streamlit
```

If I want to publish my image to my Docker.hub registry
```bash
docker image build -t afrancog54/streamlit:v1 .
```

2. Launch my image
```bash
docker run -idtP afrancog54/streamlit:v1
```

3. Remove my Docker container
```bash
docker rm -f ['CONTAINER ID']
```

3. push the image to my docker.hub
```bash
docker image push afrancog54/streamlit:v1
```
  