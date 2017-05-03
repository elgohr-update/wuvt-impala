impala
======

`impala` is the Inventory of Music for Perusal, Acquisition, and Library
Administration. This stores a catalog of album metadata stored in PostgreSQL.


Components so far
=================

- Versioned api ('/api')
- Frontend
- Catalog models


Running a dev server
====================

``
pip install -r requirements.txt
export FLASK_APP=impala
export FLASK_DEBUG=1
flask run
``

If you change the schema:
``
python3 manage.py migrate
python3 manage.py upgrade
``

TODO (in order)
===============
- API GET/PUT/POST/DELETE for each model
- AuthN
- AuthZ
- Frontend build-out 
    - Decide whether this goes here or in a separate app
    - Bootstrap!
    - Figure out how album art plays into this - MOSS? 
- uwsgi file
- Containerize
