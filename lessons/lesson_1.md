# Занятие 1

TODO
 - подготовить свой eslint  
 - Правила работы на github?  
 - Мало, надо придумать еще.  

## Теоретическая часть

### Настройка рабочей среды  
 - Правила работы с кодом на курсе  
 - Основная информация о Node.js, запуск скриптов.  
 - Что такое процесс, stdin, stdout  
 - Базовые знания о linux, bash  


## Практическая часть

### Установка и настрока
 - Установка nvm, nodejs, git, docker  
 - Установка текстового редактора (Sublime, Visual Studio Code).  
 - Настройка текстового редактора:
   - eslint (airbnb)  
   - editorconfig  
 - Регистрация на github, dockerhub  
 - Работа с npm, package.json.  

### Задание 1
???


## Homework

Реализуйте программу, которая принимает на вход один или более аргументов и
выводит их сумму в консоль (stdout).

----------------------------------------------------------------------
### ИНФОРМАЦИЯ
Вы можете получить доступ к аргументам командной строки через глобальный объект `process`. Объект `process` имеет свойство `argv`, которое представляет из себя массив аргументов командной строки, например `process.argv`.
Для начала реализуйте программу, которая содержит:

```js
console.log(process.argv)
```

Запустите ее с помощью `node program.js` добавив несколько чисел в качестве аргументов, например:

```sh
$ node program.js 1 2 3
```
В данном случае вывод должен быть массивом вида:

```js
[ 'node', '/path/to/your/program.js', '1', '2', '3' ]
```
Ваша задача пройтись по этому массиву для того чтобы Вы смогли получить сумму только переданных аргументов. Первый аргумент `process.argv` всегда `node`, второй - это путь до файла program.js, таким образом Вам нужно начать с 3го элемента (индекс 2) и добавлять каждый элемент к искомой сумме до тех пор пока не дойдете до конца массива.
Так же примите во внимание то, что все элементы `process.argv` имеют строковый тип, поэтому возможно Вам придется конвертировать их в числа. Вы можете сделать это добавлением префикса `+` к элементу или передать его в функцию `Number()` или `parseInt()`, например  `+process.argv[2]` или `Number(process.argv[2])` или `parseInt(process.argv[2])`.

