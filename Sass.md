# Sass
#### [Lesson One](https://www.codecademy.com/courses/learn-sass/lessons/hello-sass/exercises/sass-generalizations?action=lesson_resume) 
main.scss
```
$icon-square-length: 300px;
$standard-border: 4px solid black;

.icon {
  width: $icon-square-length;
  height: $icon-square-length;
}
```

main.scss
- hidden is the default value 
- change default by writing @include backface-visibility(not-hidden) in the end
```
@mixin backface-visibility($visibility: hidden) {
  backface-visibility: $visibility;
  -webkit-backface-visibility: $visibility;
  -moz-backface-visibility: $visibility;
  -ms-backface-visibility: $visibility;
  -o-backface-visibility: $visibility;
}

.front, .back {
    @include backface-visibility;
}
```
