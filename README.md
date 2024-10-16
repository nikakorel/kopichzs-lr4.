def sort_lowercase_in_array(arr):
    lowercase_letters = [char for char in arr if char.islower()]
    if lowercase_letters == sorted(lowercase_letters):
        print("Массив уже отсортирован: ", ''.join(arr))
        return
    lowercase_letters.sort()
    lowercase_index = 0
    for i in range(len(arr)):
        if arr[i].islower():
            arr[i] = lowercase_letters[lowercase_index]
            lowercase_index += 1
    print("Преобразованный массив: ", ''.join(arr))
def process_arrays(arrays):
    for arr in arrays:
        sort_lowercase_in_array(arr)

arrays = [
list("aBcDeFghIjK"),  
    list("zYxwVuTsrQpO"),  
    list("ABCDEF"),  
    list("AbCdEfGhIj"),  
    list("aBcD")  
]
