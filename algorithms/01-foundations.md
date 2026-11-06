# Основы
 Базовый поиск (бинарный), структура памяти (массивы vs списки), простые сортировки и хэш-таблицы

## 1. Бинарный поиск
Это алгоритм, который ищет элементы только на отсортированном массиве и каждый раз делит его пополам. Из-за того, что бинарный поиск отсекает половину неподходящих вариантов, время его выполнения происходит за $\log_2(n)$


**Его сложность:** <img width="82" height="43" alt="изображение" src="https://github.com/user-attachments/assets/8b16d9ba-a8b7-4b5c-8220-f9586c9ff1de" />

При бинарном поиске массив делится на 2<br/>
**Метод работы:**
каждый раз алгоритм проверяет ср. элемент<br/>
`mid = (low+high)/2`<br/>
`guess = list[mid]`

### Реализация на Python 
`def binary_search(arr, item):`<br/>
  `low = 0;`<br/>
  `high = len(arr) - 1;`<br/>

  `while low <= high:`<br/>
   ` mid = (low+high)//2;`<br/>
    `guess = arr[mid];`<br/>
    `if guess == item:`<br/>
      `return mid`<br/>
    `elif guess > item:`<br/>
    `high = mid - 1`<br/>
    `else:`<br/>
     ` low = mid + 1;`<br/>
  `return print('Такого элемента нет')`<br/>

`my_list = [1, 3, 5, 7]`<br/>

`print(binary_search(my_list, 4));`<br/>

 
