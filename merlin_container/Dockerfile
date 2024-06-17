FROM nvcr.io/nvidia/merlin/merlin-tensorflow:23.12

EXPOSE 8080

COPY merlin_container/requirements.txt .

COPY merlin_container/jupyter_notebook_config.py /root/.jupyter

ENV pwd=""
ENTRYPOINT exec jupyter-lab --ip=0.0.0.0 --port=8080 --no-browser --allow-root --ServerApp.allow_origin="*" --NotebookApp.token="$pwd" --NotebookApp.password="$pwd"
