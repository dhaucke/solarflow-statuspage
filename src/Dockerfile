FROM python:3.10

# Create stdconfig directory
WORKDIR /

COPY src/requirements.txt /
RUN pip install -r requirements.txt
COPY src/zenapi /zenapi
COPY src/static /static
COPY src/templates /templates
COPY src/solarflow-status.py /

# Inform Docker about the exposed port (optional but good practice)
EXPOSE 5000

ENTRYPOINT ["python","solarflow-status.py"]
