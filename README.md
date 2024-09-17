1. Создать пакет mathutils с функцией для вычисления факториала числа.

2.Использовать созданный пакет для вычисления факториала введенного пользователем числа.

3. Создать пакет stringutils с функцией для переворота строки и использовать его в основной программе.

4. Написать программу, которая создает массив из 5 целых чисел, заполняет его значениями и выводит их на экран.

5. Создать срез из массива и выполнить операции добавления и удаления элементов.

6. Написать программу, которая создает срез из строк и находит самую длинную строку.

folder gothird/mathutils
```
  package mathutils

  import "fmt"
  
  // task_1
  func Fact() {
  	fmt.Print("\n1st task\nEnter number: ")
  	var a int64
  	sum := int64(1)
  
  	fmt.Scan(&a)
  
  	if a == 0 {
  		fmt.Print(1)
  	} else if a > 0 {
  		for b := int64(1); b <= a; b++ {
  			sum *= b
  		}
  		fmt.Print("fact ", a, " - ", sum)
  	} else {
  		fmt.Print("Enter the positive number")
  	}
  
  }

```

folder gothird/stringutils
```
  package stringutils
  
  import "fmt"
  
  func ReverseString() {
  	fmt.Print("\n\n3rd task\nEnter text: ")
  
  	var a string
  	fmt.Scan(&a)
  
  	arr := []rune(a)
  
  	fmt.Print("reversed text - ")
  	for b := len(arr) - 1; b >= 0; b-- {
  		fmt.Print(string(arr[b]))
  	}
  }

```

main.go
```
package main

import (
	"fmt"
	"gothird/mathutils"
	"gothird/stringutils"
)

func main() {
	mathutils.Fact()
	stringutils.ReverseString()
	AddArr()
	SliceStringArr()
}

// task_4
func AddArr() {
	arr := []int{1, 2, 3, 4, 5}
	for a := 10; a < 15; a++ {
		arr = append(arr, a)
	}
	fmt.Print("\n\n4rd task\n", arr)
	SliceArr(arr)
	fmt.Print(SliceArr(arr))
}

// task_5
func SliceArr(a []int) []int {
	slice := a[2:6]
	fmt.Print("\n\n5th task\n", "sliced array: ", slice)
	slice = append(slice, 20)
	fmt.Print("\nadded 20 ", slice)
	fmt.Print("\ndeleted 1st elem ")
	return slice[1:]
}

// task_6
func SliceStringArr() {
	print("\n\n6th task\n")
	var first, second, third string

	fmt.Print("Enter 1st text: ")
	fmt.Scan(&first)
	fmt.Print("Enter 2nd text: ")
	fmt.Scan(&second)
	fmt.Print("Enter 3rd text: ")
	fmt.Scan(&third)

	arr := []string{first, second, third}
	fmt.Print("\nyour array: ", arr)

	arr[1] = "vietnam"
	fmt.Print("\nupdated array: ", arr)

	myMax := int(0)
	for i := int(0); i < len(arr); i++ {
		if len(arr[i]) > len(arr[myMax]) {
			myMax = i
		}
	}
	print("\nlongest line - ", arr[myMax])
}

```
![{033F6793-5BC1-4FFA-BC7F-E01EAD24C427}](https://github.com/user-attachments/assets/dcbafa8a-1ee4-4b1d-a4d0-033d9d0c033c)
