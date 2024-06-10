# rest-framework_guideline



- [Configuration](https://github.com/chanawit-k/rest-framework_guideline/commit/c71870a566c26703f805c4a485df15271f6f3068)

## How to use Auth Token
### setting.py
```python
    INSTALLED_APPS = [
        ...
        'rest_framework.authtoken'
        ...
    ]
```

### urls.py
```python
    from rest_framework.authtoken.views import obtain_auth_token

    urlpatterns = [
        ...
        path('api-token-auth/', obtain_auth_token)
    ]
```

### views.py
```python
    authentication_classes = [TokenAuthentication]
```