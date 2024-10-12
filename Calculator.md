## 1. Open Jupyter notebook and install pytest:
``` bash
! pip install pytest
```

``` bash
! pytest --version
```

## 2. Write the functions:
``` bash
def calc(a,s,b):
    if s=="+":
        return a+b
    elif s=="-":
        return a-b
    elif s=="*":
        return a*b
    elif s=="/":
        return a/b
    elif s=="%":
        return a%b
    else:
        return "Invalid"
```
``` bash
def test_calc():
    assert calc(5,"+",10)==15
    assert calc(10,"-",5)==5
    assert calc(5,"*",10)==50
    assert calc(10,"/",5)==2
    assert calc(10,"%",5)==0
    assert calc(10,"@",5)=="Invalid"
```

## 3. Write the above functions to a file with filename having _test:
``` bash
test_code = """
def calc(a,s,b):
    if s=="+":
        return a+b
    elif s=="-":
        return a-b
    elif s=="*":
        return a*b
    elif s=="/":
        return a/b
    elif s=="%":
        return a%b
    else:
        return "Invalid"
        
def test_calc():
    assert calc(5,"+",10)==15
    assert calc(10,"-",5)==5
    assert calc(5,"*",10)==50
    assert calc(10,"/",5)==2
    assert calc(10,"%",5)==0
"""

with open("test_calc.py", "w") as f:
    f.write(test_code)
```

## 4. Run the file:

``` bash
!pytest test_calc.py
```
