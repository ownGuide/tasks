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
    document.getElementById("cube").innerHTML = `<img src=${number}.jpg>`;
}
```

4. Заменить код в значении атрибута `onclick` тэга `button` - разместить там вызов функции `throwDie`:
```html
<button onclick="throwDie();">Бросок<button>
```
Протестировать работу кнопки (при каждом нажатии на кнопку обновляется изображение кубика)