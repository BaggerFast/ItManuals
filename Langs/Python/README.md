# How to create venv for python
Virtualenv is a tool for creating an isolated Python environment.
when you using it, the downloaded libraries aren't available to others.
This environment doesn't have access to global libraries.

### In Unix
```bash
python3 -m venv venv && source venv/bin/activate
```

### In Windows
```bash
python3 -m venv venv && .\venv\Scripts\activate
```