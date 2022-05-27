1. Добавить к [предыдущей странице](dice_game_js_1.md) кнопку:
```html
<button>Бросок<button>
```
Код, приведеный выше, добавляет на веб-страницу кнопку, но её нажатие ни к чему не приводит.  

2. Добавить к кнопке (к тэгу `button`) атрибут `onclick` со значением `alert('Привет!');`:
```html
<button onclick="alert('Привет!');">Бросок<button>
```
Убедиться, что размещенный в значении атритуба JavaScript код (`alert('Привет!');`) выполняется при каждом нажатии кнопки

3. Оформить существующий JavaScript код в виде **функции**:  
```js
function throwDie() {
    let number = Math.floor(Math.random() * 6) + 1;
    document.getElementById("result").innerHTML = `<img src=${number}.jpg>`;
}
```

4. Заменить код в значении атрибута `onclick` тэга `button` - разместить там вызов функции `throwDie`:
```html
<button onclick="throwDie();">Бросок<button>
```
Протестировать работу кнопки (при каждом нажатии на кнопку обновляется изображение кубика)

<details>
<summary>Если возникли трудности, просмотрите код здесь</summary>

```html
<!DOCTYPE html>
<html lang="ru">
    <head>
        <meta charset="utf-8">
        <title>Бросок кубика</title>
    </head>
    <body>
        <h1>Бросок кубика</h1>
        <button onclick="throwDie();">Бросок</button>
        <div id="result">
        </div>
        <script>
            function throwDie() {
                let number = Math.floor(Math.random() * 6) + 1;
                document.getElementById("result").innerHTML = `<img src="img/${number}.jpg">`;
            }
        </script>
    </body>
</html>
```
</details>