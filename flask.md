- Kill all servers still running in App.py
```
// get a list of process number 
ps aux | grep App.py

// ex process-number 53985
kill -9 PROCESS-NUMBER
```


- create env 
```sh
mkdir INTUIT APP
cd INTUIT\ /APP
virtualenv venv
. venv/bin/activate
```

- activate env
```sh
pip install flask  
```

- run flask app - http://127.0.0.1:5000/
```sh
cd Flask
python hello.py
```

- example
- post to ```http://127.0.0.1:5000/testingPost``` this ```{"Taher": "Boy", "Mona": "Girl"}``` which will show ```"Boy"```

```python
from flask import Flask, request, jsonify

app = Flask(__name__)
@app.route("/")
def index():
    return "Test"

@app.route("/another", methods=["GET", "POST"])
def another():
    value = request.json['key']
    return value

@app.route("/jsonhandle", methods=["POST"])
def jsonhandle():
    return jsonify({"result": "sucess"})

@app.route("/testingPost", methods=["POST"])
def testingPost():
    name = request.get_json()
    return jsonify(name["Taher"])


if __name__ == "__main__":
    app.run(debug=True, use_reloader=True)
```
