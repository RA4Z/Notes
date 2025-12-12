It's possible to create a [[Lists|List]] of [[Dictionaries|Dicts]] by using the following code for example:
```Python
with open(os.path.join(os.getcwd(), 'Input.txt'), 'r', encoding='utf-8') as f:  
    headers = f.readline().strip().split(';')  
    items = [{key: value for key, value in zip(headers, row.strip().split(';'))} for row in f]
```