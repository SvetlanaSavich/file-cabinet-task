# File Cabinet

## Шаг 11 - Конфигурация и журналирование

Цель: вывод отладочной и дополнительной информации.

Все изменения (commits) должны храниться в ветке _step11-add-config-and-logging_, а после окончания работы должны быть слиты в ветку _master_ (использовать squash-merge).


### Задание

#### Критерии валидации

1. Сохраните текущие критерии валидации в файл _validation-rules.json_.

Пример структуры файла:

```json
{
	"default": {
		"firstName": {
			"min": 2,
			"max": 60
		},
		"lastName": {
			"min": 2,
			"max": 60
		},
		"dateOfBirth": {
			"from": "1/1/1950",
			"to": "10/8/2019"
		}
	},
	"custom": {
		"firstName": {
			"min": 5,
			"max": 80
		},
		"lastName": {
			"min": 5,
			"max": 80
		},
		"dateOfBirth": {
			"from": "1/1/1980",
			"to": "10/8/2019"
		}
	}
}
```

#### Для .NET Core

Установите пакеты:

* Microsoft.Extensions.Configuration
* Microsoft.Extensions.Configuration.Binder
* Microsoft.Extensions.Configuration.FileExtensions
* Microsoft.Extensions.Configuration.Json

Реализуйте загрузку критериев валидации из конфигурационного файла с применением [ConfigurationBinder.Get<T>](https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration.configurationbinder.get). См. [Bind to an object graph](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration/?view=aspnetcore-3.0#bind-to-an-object-graph).


#### Для .NET Framework

Установите пакет _Newtonsoft.Json_ и реализуйте загрузку параметров через [JsonConvert.DeserializeObject](https://www.newtonsoft.com/json/help/html/SerializationAttributes.htm).

#### Журналирование работы сервиса

#### Журналирование времени работы сервиса