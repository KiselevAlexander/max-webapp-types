# @max-webapp/types

Библиотека типов TypeScript для глобального объекта window.WebApp. 
Предназначена для обеспечения строгой типизации при разработке мини-приложений для [MAX мессенджера](https://dev.max.ru/docs/webapps/introduction).

Подробное описание своиств и методов в [официальной документации MAX Bridge](https://dev.max.ru/docs/webapps/bridge)

## 🚀 Установка
Установите пакет как зависимость для разработки:

```shell
npm install --save-dev @max-webapp/types
# или
yarn add -D @max-webapp/types
```

## 🛠 Настройка

Чтобы TypeScript автоматически распознавал типы в глобальном пространстве имен `window`, добавьте пакет в ваш `tsconfig.json`:

```json
{
  "compilerOptions": {
    "types": ["@max-webapp/types"]
  }
}
```

Или импортируйте типы напрямую в вашем основном файле (например, `main.ts` или `index.ts`):

```typescript
import '@max-webapp/types';
```


## 📖 Использование

После настройки объект window.WebApp будет полностью типизирован. Вам будут доступны автодополнение и проверка типов для всех методов и свойств:

```typescript
// Пример использования в коде
const webApp = window.WebApp;

webApp.ready();

console.log(`Привет ${webApp.initDataUnsafe.user.first_name}!`);

webApp.enableClosingConfirmation();
```

## 🤝 Контрибьютинг
1. Сделайте форк репозитория.
2. Создайте ветку для вашей фичи (git checkout -b feature/AmazingFeature).
3. Закоммитьте изменения (git commit -m 'Add some AmazingFeature').
4. Отправьте ветку в репозиторий (git push origin feature/AmazingFeature).
5. Откройте Pull Request.

## 📄 Лицензия
Распространяется под лицензией MIT.