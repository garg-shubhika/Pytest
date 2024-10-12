### 1. Open terminal, make sure to install Python 

```bash
python --version
```

 ```bash
sudo apt install python-pytest
```

 ```bash
pytest --version
```

### 2. Naming convention:

- **Files**: Files that start with **test_** or end with **_test.py**.
- **Functions**: Functions that start with **test_**.

### 3. Write a Python file:

 ```bash
nano test_num.py
```

 ```bash
def func (a):
        if a%2==0:
                return "even"
        else:
                return "odd"

def test_func():
        assert func(4)=="even"
        assert func(11)=="odd"
        assert func(0)=="even"
        assert func(555)=="odd"
```

### 3. Run the file:

```bash
pytest test_num.py
```
