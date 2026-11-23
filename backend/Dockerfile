FROM python

WORKDIR /app

RUN git clone https://github.com/mmenapace/SomeBankingApp.git .

WORKDIR /app/backend

RUN pip install -r requirements.txt

ENTRYPOINT ["python", "-m", "uvicorn", "main:app"]
