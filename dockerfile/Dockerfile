# Stap 1: Gebruik een basis image met Python 3.9+
FROM python:3.9-slim

# Stap 2: Stel de werkdirectory in
WORKDIR /app

# Stap 3: Kopieer requirements.txt en installeer de benodigde packages
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Stap 4: Kopieer de app code naar de container
COPY . .

# Stap 5: Stel de FLASK_APP environment variable in
ENV FLASK_APP=app.py

# Stap 6: Expose poort 5000 zodat de app buiten de container beschikbaar is
EXPOSE 5000

# Stap 7: Start de Flask applicatie
CMD ["flask", "run", "-h", "0.0.0.0", "-p", "5000"]