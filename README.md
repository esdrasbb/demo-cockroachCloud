# demo-cockroachCloud
Demo code for cockroach cloud DB - Python version

Test psycopg with CockroachDB.

More details in https://cockroachlabs.cloud/

Source code - https://github.com/cockroachlabs/hello-world-python-psycopg2 

Some changes were made in initial code version

Importants points:

- It's necessary an account in https://cockroachlabs.cloud/

- It's necessary to create a database with 'bank' name

- Install psycopg2
```
$ pip install psycopg2-binary
```

- Console output
```
$ python demo.py "postgres://<username>:<password>@free-tier.gcp-us-central1.cockroachlabs.cloud:26257/<cluster-name>.bank?sslmode=verify-full&sslrootcert=root.crt"
INFO:root:create_accounts(): status message: INSERT 0 2
INFO:root:print_balances(): status message: SELECT 2
INFO:root:transfer_funds(): status message: UPDATE 1
INFO:root:print_balances(): status message: SELECT 2
INFO:root:delete_accounts(): status message: DELETE 2
Balances at Wed Jul  7 16:40:28 2021:
(1, 1000)
(2, 250)
Balances at Wed Jul  7 16:40:29 2021:
(1, 900)
(2, 350)
```