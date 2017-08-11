# Hug Example Using Zappa

This is a super simple hug example using zappa. The only real trick here was knowing to set
the app setting in the zappa_settings.json file. Hug provides a magic method for the wsgi compatible
server that should be given to Zappa.  

`"app_function": "app.__hug_wsgi__"`

Make sure you modify your zappa `s3_bucket` setting prior to deployment.

```bash
python -m venv env
source env/bin/activate
pip install -r requirements.txt
zappa deploy
```