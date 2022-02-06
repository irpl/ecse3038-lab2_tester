# ecse3038-lab2_tester

Demo: https://ecse3038-lab2-tester.netlify.app/

To test out your lab, you'll need to install one extra python library while your venv is active:

```
(.venv) lab2> pip install flask-cors
```

Then you'll need to import the library and initialize the extension:
```python
from flask import Flask
from flask_cors import CORS # <-- HERE

app = Flask(__name__)
CORS(app) # <-- HERE

@app.route("/")
def helloWorld():
  return "Hello, cross-origin-world!"
```

If you want to learn more about CORS: https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

Flask-CORS Documentation: https://flask-cors.readthedocs.io/en/latest/

**NOTE**: Your server must be running on port 3000 for the webapp to work.
