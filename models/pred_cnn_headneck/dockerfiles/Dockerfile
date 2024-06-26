#FROM python:3.8.8
FROM mhubai/base:latest

# Update authors label
LABEL authors="maastro.nl"

# Install the dependencies
# COPY and ADD is prohibited!!!

COPY ./requirements.txt /requirements.txt
RUN pip install -r requirements.txt
# Install the package
COPY ./hn_cnn/ /app/hn_cnn
COPY ./setup.py ./README.md /app/ 
RUN pip install --no-cache-dir /app

# Import the MHub model definiton
ARG MHUB_MODELS_REPO
RUN buildutils/import_mhub_model.sh pred_cnn_headneck ${MHUB_MODELS_REPO}
RUN -v .(path) image_name 
# Clone Source Code
???
RUB tar -xf -folder of tar - (name.tar) -C /mnt/data # unzip and mv to mnt/tar


# Pull weights into the container


# Default run script
ENTRYPOINT ["python3", "-m", "mhubio.run"]
CMD ["--workflow", "default"]