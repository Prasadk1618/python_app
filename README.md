# python app hosting with amazon Linux

  ##  steps:-
### update package manager.
 ```bash
	 sudo yum update
```
### check python virson.
```bash	
  python -v
```
### install python & virsual envornment
 ```bash
	 sudo yum install python3-venv python3-pip -y
```
### create directory
```bash
   mkdir dirname
 ```
### Go The Directory

```bash
cd dirname
```
### create virtual envornment
 ```bash
	 python3 -m venv myenv
```
### active virtual envornment
 ```bash
	 source myenv/bin/activate
```
### create requirement.txt & add list of software
 ```bash
	 nano requirement.txt
```
### install the requirement.txt
 ```bash
	 pip install -r requirement.txt
```
### create app.py file & add the app code
```bash	
  nano app.py
```
### start the GUNICORN 
 ```bash
gunicorn --bind 0.0.0.0:8000 myapp:app
```
### start or run background GUNICORN
```bash
gunicorn --workers 3 --bind 0.0.0.0:8000 myapp:app&
```
