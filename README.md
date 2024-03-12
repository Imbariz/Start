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

# Example usage:
# The array should be sorted for binary search
sorted_array = [1, 3, 5, 7, 9, 11, 13, 15, 17, 19]
target_value = 9

# Perform binary search
index = binary_search(sorted_array, target_value)

# Print the result
if index != -1:
    print(f"Element found at index {index}")
else:
    print("Element not found in the array")
