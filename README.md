# paython app hosting with amazon Linux

  ##  steps:-
### update package manager.
 ```bash
	 SUDO YUM UPDATE -Y
```
### check paython virson.
```bash	
  paython -v
```
### install paython & virsual envornment
 ```bash
	 sudo yum install paython3-venv paython3-pip -y
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
	 paython3 -m venv myenv
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
