FROM python:3.9

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5433

CMD ["uvicorn", "server:app", "--host", "0.0.0.0", "--port", "5433", "--reload"]