FROM python:3.10

# Create stdconfig directory
WORKDIR /

COPY src/requirements.txt /
RUN pip install -r requirements.txt
COPY src/zenapi /zenapi
COPY src/static /static
COPY src/templates /templates
COPY src/solarflow-status.py /


ENTRYPOINT ["python","solarflow-status.py"]
