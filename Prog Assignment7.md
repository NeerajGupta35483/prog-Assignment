1. Write a Python Program to find sum of array?


```python
def sumOfArray(l):
    print(f"Sum of {l} is {sum(l)}")
    
sumOfArray([1,2,3,4])
```

    Sum of [1, 2, 3, 4] is 10
    

2. Write a Python Program to find largest element in an array?


```python
def maxOfArray(l):
    print(f"Maximum element of {l} is {max(l)}")
    
maxOfArray([4,2,5,7,1,3])
```

    Maximum element of [4, 2, 5, 7, 1, 3] is 7
    

3. Write a Python Program for array rotation?


```python
def arrayRotation(arr_list):
    rotation_arr = []
    size_arr = len(arr_list)
    rotation = input("Enter Rotation Right/Left: ")
    rotation_number = int(input("Enter the Nummber of Elements to Rotate: "))
    
    if(rotation_number>size_arr):
        print("Rotattion Number Of Elements should be less than the Size of array list")
    else:
        if rotation.upper() == "RIGHT":
            print("The Orginal Array is: ",arr_list)
            rotation_arr = arr_list[-(rotation_number):] + arr_list[:(size_arr-rotation_number)]
            print("After Right Rotation the Array List is: ",rotation_arr)
            
        elif rotation.upper() == "LEFT":
            print("The Orginal Array is: ",arr_list)
            rotation_arr = arr_list[rotation_number:size_arr] + arr_list[:rotation_number]
            print("After Left Rotation the Array List is: ",rotation_arr)
            
            
        else:
            print("Wrong Array")
    
    

arrayRotation([1,2,3,4,5,6,7,8])
```

    Enter Rotation Right/Left: Right
    Enter the Nummber of Elements to Rotate: 4
    The Orginal Array is:  [1, 2, 3, 4, 5, 6, 7, 8]
    After Right Rotation the Array List is:  [5, 6, 7, 8, 1, 2, 3, 4]
    

4. Write a Python Program to Split the array and add the first part to the end?


```python
def splitArr(arr_list):
    split_arr = []
    new_arr = []
    size_arr = len(arr_list)
    split_num = int(input("Enter The Number of Elements to Split: "))
    if(split_num>size_arr):
        print("The split number of element must be less than size of array")
    else:
        split_arr = arr_list[:split_num]
        print("The Split Array List is: ",split_arr)
        new_arr = arr_list[split_num:] + arr_list[:split_num]
        print("The list after split and add the first part to the end: ",new_arr)
        
        
splitArr([1,2,3,4,5,6,7])  
```

    Enter The Number of Elements to Split: 3
    The Split Array List is:  [1, 2, 3]
    The list after split and add the first part to the end:  [4, 5, 6, 7, 1, 2, 3]
    

5. Write a Python Program to check if given array is Monotonic?


```python
def isMonotonic(arr_list):
    len_arr = len(arr_list)
    if all(arr_list[i]>=arr_list[i+1] for i in range(len_arr-1)) or all(arr_list[i]<=arr_list[i+1] for i in range(len_arr-1)):
        return True
    else:
        return False

```


```python
isMonotonic([6, 5, 4, 4,5])
```




    False




```python
isMonotonic([6,5,4])
```




    True


