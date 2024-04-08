# Django REST Framework

## Установка и настройка

1. Установите Django и Django REST Framework:

```
pip install django djangorestframework
```

2. Добавьте `'rest_framework'` в `INSTALLED_APPS` в файле `settings.py`:

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

## Serializers (Сериализаторы)

### Создание сериализатора

```python
from rest_framework import serializers

class ExampleSerializer(serializers.Serializer):
    id = serializers.IntegerField(read_only=True)
    name = serializers.CharField(max_length=100)
    description = serializers.CharField(required=False)
```

### Использование ModelSerializer

```python
from rest_framework import serializers
from .models import Example

class ExampleSerializer(serializers.ModelSerializer):
    class Meta:
        model = Example
        fields = ['id', 'name', 'description']
```

## Views (Представления)

### Function-based views (на основе функций)

```python
from rest_framework.decorators import api_view
from rest_framework.response import Response
from .serializers import ExampleSerializer

@api_view(['GET', 'POST'])
def example_list(request):
    if request.method == 'GET':
        examples = Example.objects.all()
        serializer = ExampleSerializer(examples, many=True)
        return Response(serializer.data)
    elif request.method == 'POST':
        serializer = ExampleSerializer(data=request.data)
        if serializer.is_valid():
            serializer.save()
            return Response(serializer.data, status=201)
        return Response(serializer.errors, status=400)
```

### Class-based views (на основе классов)

```python 
from rest_framework import generics
from .models import Example
from .serializers import ExampleSerializer

class ExampleList(generics.ListCreateAPIView):
    queryset = Example.objects.all()
    serializer_class = ExampleSerializer

class ExampleDetail(generics.RetrieveUpdateDestroyAPIView):
    queryset = Example.objects.all()
    serializer_class = ExampleSerializer
```

## URL patterns (Маршрутизация)

```python
from django.urls import path
from .views import ExampleList, ExampleDetail

urlpatterns = [
    path('examples/', ExampleList.as_view(), name='example-list'),
    path('examples/<int:pk>/', ExampleDetail.as_view(), name='example-detail'),
]
```
