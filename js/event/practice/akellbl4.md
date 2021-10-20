🛠 В событии есть два похожих поля: `target` и `currentTarget`. Их отличие можно легко увидеть на практике.

Создадим кнопку и положим в неё текст, обёрнутый в тег `<span>`. И навесим обработчик событий на кнопку. При клике на кнопку можно заметить, что `currentTarget` всегда будет одним и тем же, то есть кнопка, на которой слушается событие. При этом `target` будет меняться в зависимости от того, куда на кнопке мы кликнули: на элемент внутри кнопки или на неё саму, так как там всегда содержится указатель на элемент, на котором произошло событие.

```html
<button class="button" type="button">
  <span>Моя кнопочка</div>
</button>
```

```js
document.querySelector('.button').addEventListener('click', function (event) {
  console.log('Событие инициированно на', event.target)
  console.log('Событие поймано на', event.currentTarget)
})
```

<iframe title="Разница между target и currentTarget" src="../demos/target-vs-currenttarget/" height="150"></iframe>
