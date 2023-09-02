# EN
## Foodgram Project – Grocery Assistant

### On this service, users will be able to publish recipes, subscribe
to other users' publications, etc.

### The user can also create a list of products and add the ingredients needed for the recipe there.

- Cloning a remote repository
```bash
git clone git@github.com:Danila747/foodgram-project-react.git
cd infra
```
- In the /infra directory, create a .env file with environment variables like .env.example
- Container assembly
```bash
docker-compose up -d --build
```
```bash
docker-compose exec backend python manage.py makemigrations
docker-compose exec backend python manage.py migrate
docker-compose exec backend python manage.py collectstatic --no-input
docker-compose exec backend python manage.py createsuperuser
```
- FIll the database
```bash
docker-compose exec backend python manage.py load_data
```

### Запуск проекта локально

```bash
cd backend
python -m venv venv
source venv/Scripts/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```
```bash
python manage.py makemigrations
python manage.py migrate
python manage.py collectstatic --noinput
```
- Fill the database
```bash
python manage.py load_data
```

- Start the server
```bash
python manage.py runserver 
```

# DE
## Das Foodgram-Projekt ist ein Lebensmittelassistent

### Auf diesem Dienst können Benutzer Rezepte veröffentlichen, abonnieren 
auf die Veröffentlichung anderer Benutzer usw.

###

- Klonen eines Remote-Repositorys
```bash
git clone git@github.com:Danila747/foodgram-project-react.git
cd infra
```
- Erstellen Sie im Verzeichnis /infra eine Datei.env, mit Umgebungsvariablen wie .env.example
- Montage von Containern
```bash
docker-compose up -d --build
```
```bash
docker-compose exec backend python manage.py makemigrations
docker-compose exec backend python manage.py migrate
docker-compose exec backend python manage.py collectstatic --no-input
docker-compose exec backend python manage.py createsuperuser
```
- Füllen Sie die Datenbank aus
```bash
docker-compose exec backend python manage.py load_data
```
- oder füllen Sie die Datenbank mit Testdaten aus
```bash
docker-compose exec backend python manage.py loaddata data/data.json 
```
#### Führen Sie das Projekt lokal aus

```bash
cd backend
python -m venv venv
source venv/Scripts/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```
```bash
python manage.py makemigrations
python manage.py migrate
python manage.py collectstatic --noinput
```
- Füllen Sie die Datenbank aus
```bash
python manage.py load_data
```

- Starten des Servers
```bash
python manage.py runserver 
```
