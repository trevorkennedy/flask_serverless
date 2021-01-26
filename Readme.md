python3 -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt

setx USERS_TABLE users-table-dev
python app.py

npm init
npm install serverless-wsgi
npm install serverless-python-requirements
serverless login
serverless deploy

serverless logs -f app
serverless wsgi serve