# Checkmate 2019

## Setting Up Backend

### Setup Python3 and venv

- Refer this [digitalocean tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-ubuntu-16-04)

- Create a python3 virtual environment

  ```bash
  cd backend
  python3 -m venv checkmate-env
  source checkmate-env/bin/activate
  ```

- Check that the virtual environment points to correct python path
  
```bash
which python
```

- Install dependancies
  
```bash
pip install -r requirements.txt
```

### Apply Migrations

```bash
cd Checkmate2019/
python manage.py makemigrations
python manage.py makemigrations Base
python manage.py migrate
python manage.py migrate Base
```

### Populate the Database

```bash
python3 manage.py loaddata populate.json
```

### Run the server

```bash
python manage.py runserver 0.0.0.0:8000
```
## Points to note

- If you want to access the admin interface at http://localhost:8000/admin , use the username and password , both as "admin" (without quotes).
- If you want to logout in the midway, you can do so by typing either "admin" or "#" ( both without quotes) in administrator password field. 

## Contribution

- Please raise issues if the above procedure does not work for your system.
- Feel free to make necessary changes.
- Please migrate before running the server.
