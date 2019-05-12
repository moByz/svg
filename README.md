# SVG графика
## https://www.sarasoueidan.com/tags/svg/
## https://developer.mozilla.org/ru/docs/Web/SVG/Tutorial/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D0%B5_%D0%A4%D0%B8%D0%B3%D1%83%D1%80%D1%8B
```
SVG — это формат векторной графики. В отличие от растровой графики — PNG, GIF, JPEG — SVG может растягиваться и сжиматься без потери качества, то есть такие картинки будут одинаково чёткими и на обычных экранах, и на ретине.
```
## Способы вставки SVG
### Через тег img
```
<img src="picture.svg" alt="За стеклом">
```
* Не будут работать скрипты
```
Такой способ подходит изображениям, с которыми не нужно взаимодействовать
```
### Фоновая картинка в CSS
```
.picture {
  background-image:
    url(picture.svg);
}
```
* Не будут работать скрипты
```
Такой способ подходит для оформительской графики, с котороми не нужно взаимодействовать
```
### Через object
```
<object type="image/svg+xml" data="image.svg" width="200" height="200" >
  <img src="SvgImg.png" width="200" height="200" alt="image format png" />
</object
```
* Можно взаимодействовать
* Можно вставить альтернативную картинку, если браузер не поддерживает SVG
### Через svg
```
<svg
  width="20"
  height="20">
    <rect fill="#fc0"
      width="20"
      height="20"/>
</svg>
```
* Можно делать все, что и с обычными html элементами (стили, скрипты)
* Не кешируются отдельно от страницы
## Элементы
### Круг
```
<svg>
  <circle r="50" cx="50%" cy="50%" fill="yellowgreen"/>
</svg>
```
### Прямоугольник
```
<svg>
  <rect width="50%" height="100" fill="orange" />
</svg>
```
### Эллипс
```
<svg>
  <ellipse cx="75" cy="75" rx="20" ry="20" fill="#000" />
</svg>
```
### Линия
```
<svg>
  <line x1="10" x2="50" y1="110" y2="150" fill="#000" />
</svg>
```
### Ломаная линия
```
<svg>
  <polyline points="0,100 50,25 50,75 100,0" />

  <polyline points="100,100 150,25 150,75 200,0"
            fill="none" stroke="black" />
</svg>
```
### Многоугольник
```
<svg viewBox="0 0 200 100" xmlns="http://www.w3.org/2000/svg">
  <polygon points="0,100 50,25 50,75 100,0" />
  
  <polygon points="100,100 150,25 150,75 200,0"
            fill="none" stroke="black" />
</svg>
```
### Путь
```
<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <path d="M 10,30
           A 20,20 0,0,1 50,30
           A 20,20 0,0,1 90,30
           Q 90,60 50,90
           Q 10,60 10,30 z"/>
</svg>
```
### Координаты
* x - координты по оси x
* y - координаты по оси y
```
<svg>
  <rect width="50%" height="100" x="25%" y="25" stroke="orange" />
</svg>
```
### Скругление углов
* rx - скругление по оси x 
* ry - скругление по оси y
```
<svg>
  <rect width="50%" height="100" x="25%" y="25" fill="orange" rx="20" ry="50" />
</svg>
```
### Атрибуты 
* fill - задает цвет
* width - задает ширину
* height - задает высоту
