# Створення простого браузера

## Завдання "Написати простий браузер"

Вся практична виконувалась згідно методичним рекомендаціям, тому сенсу повторювати те що вже й так є немає, покажу лише невелику частину того я доповнила цей додаток

Додала метод shouldOverrideUrlLoading:
```java
@Override
public boolean shouldOverrideUrlLoading(WebView view, String url) {
    if (url.contains("www.google.")) {
        view.loadUrl(url);
        return true;
    } else {
        startActivity(new Intent(Intent.ACTION_VIEW, Uri.parse(url)));
        return true;
    }
  }
});
```

Результат виконання програми


https://github.com/katushhiaa/PR9/assets/113555695/556f2213-762e-4465-a06d-cf688d4da9d2

