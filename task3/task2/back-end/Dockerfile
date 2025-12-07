FROM ubuntu:latest

# Sistemi yenileyirik
RUN apt-get update && apt-get upgrade -y

# Python ve pip qurasdiririq
RUN apt-get install -y python3 python3-pip

# 'Externally managed' xetasini duzeldirik (Ubuntu 23+ ucun vacibdir)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Flask qurasdiririq
RUN pip3 install flask

# Is qovlugunu teyin edirik
WORKDIR /app

# Fayli konteynere kopyalayiriq
COPY ./api.py /app/api.py

# Serveri ise salirik
CMD ["python3", "api.py"]
