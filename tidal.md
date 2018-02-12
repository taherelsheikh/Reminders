Tidal GET requests

- http://127.0.0.1:5000/experiments/ids/09b3d3d4-610e-43da-afed-62aa20b3db8f

```python
@app.route('/experiments/ids/<experimentid>', methods=['GET'])
def experiment_id_availability_testing(experimentid):
    conn_info = {'host':'sbg-vertica01-prd.intuit.net',
                     'port':            5433,
                     'user':            "telsheikh",
                     'password':        "Gold4347",
                     'database':        'IDEA',
                     'unicode_error':   'strict',
                     'ssl':             False
                     }
    connection = vertica_python.connect(**conn_info)
    sql_query = ("select experiment_id from sbg_sandbox.egexperimentsids where experiment_id = %s%s%s") % ("'",experimentid, "'")
    try :
        data = pd.read_sql(sql=sql_query, con=connection)
    finally:
        connection.close()
    if data.empty :
         return jsonify(False)
    else:
         return jsonify(True)
```

- http://127.0.0.1:5000/experimentz/ids?id=09b3d3d4-610e-43da-afed-62aa20b3db8f

```python
@app.route('/experimentz/ids', methods=['GET'])
def experiment_id_available():
    experimentid = request.args.get("id")
    conn_info = {'host':'sbg-vertica01-prd.intuit.net',
                     'port':            5433,
                     'user':            "telsheikh",
                     'password':        "Gold4347",
                     'database':        'IDEA',
                     'unicode_error':   'strict',
                     'ssl':             False
                     }
    connection = vertica_python.connect(**conn_info)
    sql_query = ("select experiment_id from sbg_sandbox.egexperimentsids where experiment_id = %s%s%s") % ("'",experimentid, "'")
    try :
        data = pd.read_sql(sql=sql_query, con=connection)
    finally:
        connection.close()
    if data.empty :
         return jsonify(False)
    else:
         return jsonify(True)
```

