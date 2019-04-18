# Ejemplo del instructivo "First steps with Celery"

Pasos previos:

```bash
$ docker run -d -p 5462:5462 rabbitmq
$ pip install celery
$ celery -A tasks worker --loglevel=info
```

En otra terminal:
```python
>>> from tasks import add
>>> result = add.delay(4, 4)
>>> result.get(timeout=1)
8
```

Ver:

http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html#keeping-results
