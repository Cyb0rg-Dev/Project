def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1

# Exemplo de uso
my_list = [1, 3, 5, 7, 9, 11, 13, 15]
target_value = 9

result = binary_search(my_list, target_value)
if result != -1:
    print(f"Elemento {target_value} encontrado na posição {result}.")
else:
    print(f"Elemento {target_value} não encontrado.")
