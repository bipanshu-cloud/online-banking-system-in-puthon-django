Online Banking System V2.0.2
This is an Online Banking Concept created using Django Web Framework.

Features
Create Bank Account.
Deposit & Withdraw Money
Bank Account Type Support (e.g. Current Account, Savings Account)
Interest calculation depending on the Bank Account type
Transaction report with a date range filter
See balance after every transaction in the Transaction Report
Calculate Monthly Interest Using Celery Scheduled tasks
More efficient and accurate interest calculation and balance update
Ability to add Minimum and Maximum Transaction amount restriction
Modern UI with Tailwind CSS
Prerequisites
Be sure you have the following installed on your development machine:

Python >= 3.7
Redis Server
Git
pip
Virtualenv (virtualenvwrapper is recommended)
Requirements
celery==4.4.7
Django==3.2
django-celery-beat==2.0.0
python-dateutil==2.8.1
redis==3.5.3
Install Redis Server
Redis Quick Start

Run Redis server

redis-server
Project Installation
To setup a local development environment:

Create a virtual environment in which to install Python pip packages. With virtualenv,

virtualenv venv            # create a virtualenv
source venv/bin/activate   # activate the Python virtualenv 
or with virtualenvwrapper,

mkvirtualenv -p python3 {{project_name}}   # create and activate environment
workon {{project_name}}   # reactivate existing environment
Clone GitHub Project,

cd banking-system
Install development dependencies,

pip install -r requirements.txt
Migrate Database,

python manage.py migrate
Run the web application locally,

python manage.py runserver # 127.0.0.1:8000
Create Superuser,

python manage.py createsuperuser
Run Celery (Different Terminal Window with Virtual Environment Activated)

celery -A banking_system worker -l info

