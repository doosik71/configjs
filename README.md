# configjs

configjs is a Python package designed to simplify the process of reading and accessing configuration settings stored in a JSON file.
With configjs, you can effortlessly load a "config.json" file from the working directory and access its contents using the package name as attributes.

## Installation

Install configjs using pip:

```bash
pip install configjs
```

## Usage

- Create a "config.json" file in your project's working directory with the desired configuration settings in JSON format:

```json
{
  "database": {
    "host": "localhost",
    "port": 5432,
    "username": "user",
    "password": "secret"
  },
  "api_key": "your_api_key"
}
```

- Import and use configjs in your Python code:

```python
from configjs import Config

# Load the "config.json" file
config = Config()

# Access configuration settings using the package name as attributes
db_host = config.database.host
db_port = config.database.port
db_username = config.database.username
db_password = config.database.password
api_key = config.api_key

print(f"Database Host: {db_host}")
print(f"Database Port: {db_port}")
print(f"Database Username: {db_username}")
print(f"Database Password: {db_password}")
print(f"API Key: {api_key}")
```

- Replace the attribute names (database, host, port, username, password, api_key) with your actual configuration structure.

## Notes

configjs assumes that the "config.json" file is in the working directory.
The package name itself (config) is used as the top-level attribute to access the configuration settings.
Feel free to customize "config.json" based on your project's needs and easily manage your configuration settings using configjs.
