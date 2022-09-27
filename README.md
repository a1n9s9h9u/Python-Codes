## Python Codes

#### Element-Wise Addition of Two Lists in Python
```python
list1 = [11, 21, 34, 12, 31, 77] 
list2 = [23, 25, 54, 24, 20] 

result = [sum(i) for i in zip(list1, list2)]
```
Resultant list : [34, 46, 88, 36, 51]

zip_longest() takes two lists and fillvalue as arguments. If one of the lists is printed fully, the remaining values are filled by the values assigned to fillvalue parameter.
```python
from itertools import zip_longest

list1 = [11, 21, 34, 12, 31, 77] 
list2 = [23, 25, 54, 24, 20] 

result = [sum(x) for x in zip_longest(list1, list2, fillvalue=0)]
```
Resultant list : [34, 46, 88, 36, 51, 77]

#### Count digits in a number

Given an integer N , write program to count number of digits in N.

Input: N = 12345
Output: 5
Explanation: N has 5 digits
```python
def count_digits(n):
       count=0
       x=n
       while( x != 0 ):
               x//=10
               count+=1
       return count
```
Time Complexity: O (n) where n is the number of digits in the given integer
Space Complexity: O(1)
```python
def count_digits(n):
  x = str(n)
return len(x)
```
Time Complexity: O (1) 
Space Complexity: O(1)
```python
import math
def count_digits(n):
  digits = math.floor(math.log10(n) + 1)
return digits
```
Time Complexity: O (1) 
Space Complexity: O(1)

#### Reverse a number

Given a number N reverse the number and print it.

Input: N = 123
Output: 321
Explanation: The reverse of 123 is 321
```python
def reversDigits(num):
    string = str(num)
    string = string[::-1]
    num = int(string)
    return num
```
Time Complexity: O(n), where n is the input number
Auxiliary Space: O(1)
```python
def reversDigits(n):
    rev = 0
    while(n > 0):
        a = n % 10
        rev = rev * 10 + a
        n = n // 10
    retrn rev
```
Time Complexity: O(n), where n is the input number. 
Auxiliary Space: O(1)

#### Check if a number is Palindrome or Not

Given a number check if it is a palindrome.
An integer is considered a palindrome when it reads the same backward as forward.

Input: N =  121 
Output: Palindrome Number
Explanation: 121 read backwards as 121.Since these are two same numbers 121 is a palindrome.

Reverse the number (check previous question) and then check if they are same.

Time Complexity: O(n), where n is the input number. 
Auxiliary Space: O(1)
```python
def isPalindrome(n):
    return str(test_number) == str(test_number)[::-1]
```
Time Complexity: O(n), where n is the input number. 
Auxiliary Space: O(1)

#### Find GCD of two numbers

Input: num1 = 4, num2 = 8
Output: 4
Explanation: Since 4 is the greatest number which divides both num1 and num2.
```python
import math
print(math.gcd(num1, num2))
```
```python
def hcf(a, b):
    if(b == 0):
        return a
    else:
        return hcf(b, a % b)
```
Time Complexity: O(log(min(a,b))
Auxiliary Space: O(log(min(a,b))

#### Program to find LCM of two numbers

LCM (Least Common Multiple) of two numbers is the smallest number which can be divided by both numbers.
```python
def hcf(a, b):
    if(b == 0):
        return a
    else:
        return hcf(b, a % b)

def lcm(a,b):
    return (a / hcf(a,b))* b
```
Time Complexity: O(log(min(a,b))
Auxiliary Space: O(log(min(a,b))

#### Check if a number is Armstrong Number or not

Input:153 
Output: Yes, it is an Armstrong Number
Explanation: 1^3 + 5^3 + 3^3 = 153
```python
n = 153  # or n=int(input()) -> taking input from user
s = n  # assigning input value to the s variable
b = len(str(n))
sum1 = 0
while n != 0:
    r = n % 10
    sum1 = sum1+(r**b)
    n = n//10
if s == sum1:
    print("The given number", s, "is armstrong number")
else:
    print("The given number", s, "is not armstrong number")
```
Time complexity: O(logn)
Auxiliary Space: O(1)

#### Program to Check Whether a Number is Prime or not

Input:  n = 11
Output: True
```python
num = 11
# If given number is greater than 1
if num > 1:
    # Iterate from 2 to n / 2
    for i in range(2, int(num/2)+1):
        # If num is divisible by any number between
        # 2 and n / 2, it is not prime
        if (num % i) == 0:
            print(num, "is not a prime number")
            break
    else:
        print(num, "is a prime number")
else:
    print(num, "is not a prime number")
```
We can check till √n to make it faster
```python
from math import sqrt
# n is the number to be check whether it is prime or not
n = 1
 
# this flag maintains status whether the n is prime or not
prime_flag = 0
 
if(n > 1):
    for i in range(2, int(sqrt(n)) + 1):
        if (n % i == 0):
            prime_flag = 1
            break
    if (prime_flag == 0):
        print("True")
    else:
        print("False")
else:
    print("False")
```
#### Print all Divisors of a given Number

Input: n = 36
Output: 1 2 3 4 6 9 12 18 36
Explanation: All the divisors of 36 are printed.
```python
def printDivisors(n) :
    i = 1
    while i <= n :
        if (n % i==0) :
            print (i,end=" ")
        i = i + 1
```
Time Complexity : O(n) 
Auxiliary Space : O(1)

#### Sum of first N Natural Numbers

Input: N=5
Output: 15
Explanation: 1+2+3+4+5=15
```python
num = 16

if num < 0:
   print("Enter a positive number")
else:
   sum = 0
   # use while loop to iterate until zero
   while(num > 0):
       sum += num
       num -= 1
   print("The sum is", sum)
```
We could have solved the above problem without using a loop by using the following formula.
```python
n*(n+1)/2
```
#### Reverse a given Array
```python
lst = [10, 11, 12, 13, 14, 15]
lst.reverse()
print("Using reverse() ", lst)
 ```
 ```python
print("Using reversed() ", list(reversed(lst)))
```
```python
def Reverse(lst):
    new_lst = lst[::-1]
    return new_lst
```
#### Program for n-th Fibonacci number
```python
def Fibonacci(n):
    if n<= 0:
        print("Incorrect input")
    # First Fibonacci number is 0
    elif n == 1:
        return 0
    # Second Fibonacci number is 1
    elif n == 2:
        return 1
    else:
        return Fibonacci(n-1)+Fibonacci(n-2)
```
#### Program to display the Fibonacci sequence up to n-th term
```python
nterms = int(input("How many terms? "))

# first two terms
n1, n2 = 0, 1
count = 0

# check if the number of terms is valid
if nterms <= 0:
   print("Please enter a positive integer")
# if there is only one term, return n1
elif nterms == 1:
   print("Fibonacci sequence upto",nterms,":")
   print(n1)
# generate fibonacci sequence
else:
   print("Fibonacci sequence:")
   while count < nterms:
       print(n1)
       nth = n1 + n2
       # update values
       n1 = n2
       n2 = nth
       count += 1
```
#### Count frequency of each element in the array
```python
# intializing the list
arr = [1, 1, 1, 2, 2, 2, 2, 3, 3, 3, 3, 3]
# initializing dict to store frequency of each element
elements_count = {}
# iterating over the elements for frequency
for element in arr:
   # checking whether it is in the dict or not
   if element in elements_count:
      # incerementing the count by 1
      elements_count[element] += 1
   else:
      # setting the count to 1
      elements_count[element] = 1
# printing the elements frequencies
for key, value in elements_count.items():
   print(f"{key}: {value}")
```
We can also use collections module
```python
# importing the collections module
import collections
# intializing the arr
arr = [1, 1, 1, 2, 2, 2, 2, 3, 3, 3, 3, 3]
# getting the elements frequencies using Counter class
elements_count = collections.Counter(arr)
# printing the element and the frequency
for key, value in elements_count.items():
   print(f"{key}: {value}")
```
```python
import statistics
from statistics import mode
 
def most_common(List):
    return(mode(List))
```
Or
```python
def most_frequent(List):
    counter = 0
    num = List[0]
     
    for i in List:
        curr_frequency = List.count(i)
        if(curr_frequency> counter):
            counter = curr_frequency
            num = i
 
    return num
```
#### Program to find largest element in an array

Input : arr[] = {20, 10, 20, 4, 100}
Output : 100
```python
def largest(arr, n):
 
    # Initialize maximum element
    max = arr[0]
 
    # Traverse array elements from second
    # and compare every element with
    # current max
    for i in range(1, n):
        if arr[i] > max:
            max = arr[i]
    return max
```
Time Complexity: O(N)
Auxiliary Space: O(1)
```python
def largest(arr, n):
    ans = max(arr)
    return ans
```
#### Program to find second largest number in a list

Input: list1 = [10, 20, 4]
Output: 10
```python
# List of numbers
list1 = [10, 20, 20, 4, 45, 45, 45, 99, 99]
 
# Removing duplicates from the list
list2 = list(set(list1))
 
# Sorting the  list
list2.sort()
 
# Printing the second last element
print("Second largest element is:", list2[-2])
```
Or
```python
# List of numbers
list1 = [10, 20, 4, 45, 99]
 
# new_list is a set of list1
new_list = set(list1)
 
# Removing the largest element from temp list
new_list.remove(max(new_list))
 
# Elements in original list are not changed
# print(list1)
print(max(new_list))
```
Or
```python
def findLargest(arr):
    secondLargest = 0
    largest = min(arr)
 
    for i in range(len(arr)):
        if arr[i] > largest:
            secondLargest = largest
            largest = arr[i]
        else:
            secondLargest = max(secondLargest, arr[i])
 
    # Returning second largest element
    return secondLargest
```
#### Check if list is sorted or not
```python
# initializing list
test_list = [1, 4, 5, 8, 10]
  
# printing original list 
print ("Original list : " + str(test_list))
  
# using naive method to 
# check sorted list 
flag = 0
i = 1
while i < len(test_list):
    if(test_list[i] < test_list[i - 1]):
        flag = 1
    i += 1
      
# printing result
if (not flag) :
    print ("Yes, List is sorted.")
else :
    print ("No, List is not sorted.")
```
Or
```python
# initializing list
test_list = [10, 4, 5, 8, 10]
  
# printing original list 
print ("Original list : " + str(test_list))
  
# using sort() to 
# check sorted list 
flag = 0
test_list1 = test_list[:]
test_list1.sort()
if (test_list1 == test_list):
    flag = 1
      
# printing result
if (flag) :
    print ("Yes, List is sorted.")
else :
    print ("No, List is not sorted.")
```
sort() method time complexity O(nlogn)

#### Remove duplicates from sorted array

Input  : arr[] = {1, 2, 2, 3, 4, 4, 4, 5, 5}
Output : arr[] = {1, 2, 3, 4, 5}
         new size = 5
```python
def removeDuplicates(self, nums):
      if len(nums) == 0:
         return 0
      length = 1
      previous = nums[0]
      index = 1
      for i in range(1,len(nums)):
         if nums[i] != previous:
            length += 1
            previous = nums[i]
            nums[index] = nums[i]
            index+=1
      return length
```
Time: O(n)
O(1) extra space

#### Program for array rotation

Write a function rotate(ar[], d, n) that rotates arr[] of size n by d elements. 
```python
def rotateList(arr,d,n):
  arr[:]=arr[d:n]+arr[0:d]
  return arr
```
#### Move all zeroes to end of array

Input :  arr[] = {1, 2, 0, 4, 3, 0, 5, 0};
Output : arr[] = {1, 2, 4, 3, 5, 0, 0, 0};
```python
A = [5, 6, 0, 4, 6, 0, 9, 0, 8]
n = len(A)
j = 0
for i in range(n):
    if A[i] != 0:
        A[j], A[i] = A[i], A[j]  # Partitioning the array
        j += 1
print(A)  # Print the array
```
Time Complexity: O(N), where N is the size of elements of the input array.
Auxiliary Space: O(1) 

Or
```python
# Given list
arr = [5, 6, 0, 4, 6, 0, 9, 0, 8]
 
# Storing all non zero values
nonZeroValues = [x for x in arr if x != 0]
 
# Storing all zeroes
zeroes = [j for j in arr if j == 0]
 
# Updating the answer
arr = nonZeroValues + zeroes
 
# Printing the answer
print( "array after shifting zeros to right side: " + arr)
```
Time complexity: O(N), where N is the size of elements of the input array.
Auxiliary space: O(1).

#### Program to Search an Element in Sorted Array

Input: list1 = [4, 5, 6, 7, 0, 1, 2], target = 0
Output: 4
```python
def binarySearch(arr, l, r, x):
 
    # Check base case
    if r >= l:
 
        mid = l + (r - l) // 2
 
        # If element is present at the middle itself
        if arr[mid] == x:
            return mid
 
        # If element is smaller than mid, then it
        # can only be present in left subarray
        elif arr[mid] > x:
            return binarySearch(arr, l, mid-1, x)
 
        # Else the element can only be present
        # in right subarray
        else:
            return binarySearch(arr, mid + 1, r, x)
 
    else:
        # Element is not present in the array
        return -1
```
Time Complexity: O(log n)
Auxiliary Space: O(log n)

Or
```python
def binarySearch(v, To_Find):
    lo = 0
    hi = len(v) - 1
 
    # This below check covers all cases , so need to check
    # for mid=lo-(hi-lo)/2
    while hi - lo > 1:
        mid = (hi + lo) // 2
        if v[mid] < To_Find:
            lo = mid + 1
        else:
            hi = mid
 
    if v[lo] == To_Find:
        print("Found At Index", lo)
    elif v[hi] == To_Find:
        print("Found At Index", hi)
    else:
        print("Not Found")
```
Time Complexity: O (log n)
Auxiliary Space: O (1)

#### Union and Intersection of two sorted arrays

Input: arr1[] = {1, 3, 4, 5, 7}
        arr2[] = {2, 3, 5, 6} 
Output: Union : {1, 2, 3, 4, 5, 6, 7} 
         Intersection : {3, 5}
```python
def printUnion(arr1, arr2, m, n):
    i, j = 0, 0
    while i < m and j < n:
        if arr1[i] < arr2[j]:
            print(arr1[i],end=" ")
            i += 1
        elif arr2[j] < arr1[i]:
            print(arr2[j],end=" ")
            j+= 1
        else:
            print(arr2[j],end=" ")
            j += 1
            i += 1
 
    # Print remaining elements of the larger array
    while i < m:
        print(arr1[i],end=" ")
        i += 1
 
    while j < n:
        print(arr2[j],end=" ")
        j += 1
```
Time Complexity : O(m + n)
Auxiliary Space: O(1)

#### Handling duplicates in any of the arrays
```python
def union_array(arr1, arr2):
    m = len(arr1)
    n = len(arr2)
    i = 0
    j = 0
     
    # keep track of last element to avoid duplicates
    prev = None
     
    while i < m and j < n:
        if arr1[i] < arr2[j]:
            if arr1[i] != prev:
                print(arr1[i], end=' ')
                prev = arr1[i]
            i += 1
        elif arr1[i] > arr2[j]:
            if arr2[j] != prev:
                print(arr2[j], end=' ')
                prev = arr2[j]
            j += 1
        else:
            if arr1[i] != prev:
                print(arr1[i], end=' ')
                prev = arr1[i]
            i += 1
            j += 1
             
    while i < m:
        if arr1[i] != prev:
            print(arr1[i], end=' ')
            prev = arr1[i]
        i += 1
 
    while j < n:
        if arr2[j] != prev:
            print(arr2[j], end=' ')
            prev = arr2[j]
        j += 1
```
Time Complexity: O(l1 + l2) 
Auxiliary Space: O(n)
```python
def printIntersection(arr1, arr2, m, n):
    i, j = 0, 0
    while i < m and j < n:
        if arr1[i] < arr2[j]:
            i += 1
        elif arr2[j] < arr1[i]:
            j+= 1
        else:
            print(arr2[j],end=" ")
            j += 1
            i += 1
```
Time Complexity : O(m + n)
Auxiliary Space: O(1)

#### Find the Missing Number

Input: arr[] = {1, 2, 4, 6, 3, 7, 8}, N = 8
Output: 5
Explanation: The missing number between 1 to 8 is 5
```python
def getMissingNo(arr, n):
    total = (n + 1)*(n + 2)/2
    sum_of_A = sum(arr)
    return total - sum_of_A
```
Time Complexity: O(N)
Auxiliary Space: O(1)

#### Modification for Overflow
```python
def getMissingNo(a, n):
    i, total = 0, 1
 
    for i in range(2, n + 2):
        total += i
        total -= a[i - 2]
    return total
```
Time Complexity: O(N).  Only one traversal of the array is needed.
Auxiliary Space: O(1). No extra space is needed

#### Find the element that appears once

Input: arr[] = {12, 1, 12, 3, 12, 1, 1, 2, 3, 3} 
Output: 2 
```python
arr = [3, 3, 2, 3]
for i in arr:
    if(arr.count(i)==1):
        x=i
        break
print("The element with single occurrence is ",x)
```
#### Search elements in a Matrix
```python
# initializing list
test_list = [[4, 5, 6],
             [10, 2, 13],
             [1, 11, 18]]
  
# printing original list 
print("The original list : " + str(test_list))
  
# using any() + list comprehension
# to Search in Matrix
res = any(13 in sub for sub in test_list)
  
# printing result
print("Is 13 present in Matrix ? : " + str(res))
```
#### Sort an array of 0s, 1s and 2s

Input: {0, 1, 2, 0, 1, 2}
Output: {0, 0, 1, 1, 2, 2}
```python
def printArr(arr, n):
    for i in range(n):
        print(arr[i], end=" ") 
 
# Function to sort the array of 0s, 1s and 2s
def sortArr(arr, n):
    cnt0 = 0
    cnt1 = 0
    cnt2 = 0
 
    # Count the number of 0s, 1s and 2s in the array
    for i in range(n):
        if arr[i] == 0:
            cnt0 += 1
 
        elif arr[i] == 1:
            cnt1 += 1
 
        elif arr[i] == 2:
            cnt2 += 1
 
    # Update the array
    i = 0
 
    # Store all the 0s in the beginning
    while (cnt0 > 0):
        arr[i] = 0
        i += 1
        cnt0 -= 1
 
    # Then all the 1s
    while (cnt1 > 0):
        arr[i] = 1
        i += 1
        cnt1 -= 1
 
    # Finally all the 2s
    while (cnt2 > 0):
        arr[i] = 2
        i += 1
        cnt2 -= 1
 
    # Print the sorted array
    printArr(arr, n)
```
Time Complexity: O(n)
Space Complexity: O(1)

#### Majority Element

Input : {3, 3, 4, 2, 4, 4, 2, 4, 4}
Output : 4
Explanation: The frequency of 4 is 5 which is greater than the half of the size of the array size. 
```python
def findMajority(arr, size):
    m = {}
    for i in range(size):
        if arr[i] in m:
            m[arr[i]] += 1
        else:
            m[arr[i]] = 1
    count = 0
    for key in m:
        if m[key] > size / 2:
            count = 1
            print("Majority found :-",key)
            break
    if(count == 0):
        print("No Majority element")
```
Time Complexity: O(n)
Auxiliary Space: O(n)

Or
```python
def findMajority(arr, n):
 
    maxCount = 0
    index = -1  # sentinels
    for i in range(n):
 
        count = 0
        for j in range(n):
 
            if(arr[i] == arr[j]):
                count += 1
 
        # update maxCount if count of
        # current element is greater
        if(count > maxCount):
 
            maxCount = count
            index = i
 
    # if maxCount is greater than n/2
    # return the corresponding element
    if (maxCount > n//2):
        print(arr[index])
 
    else:
        print("No Majority Element")
```
Time Complexity: O(n*n)
Auxiliary Space: O(1)

#### Largest Sum Contiguous Subarray (Kadane’s Algorithm)
```python
def maxSubArraySum(a,size):
      
    max_so_far = a[0]
    max_ending_here = 0
      
    for i in range(0, size):
        max_ending_here = max_ending_here + a[i]
        if max_ending_here < 0:
            max_ending_here = 0
          
        # Do not compare for all elements. Compare only   
        # when  max_ending_here > 0
        elif (max_so_far < max_ending_here):
            max_so_far = max_ending_here
              
    return max_so_far
```
Time Complexity: O(n)
Auxiliary Space: O(1)

#### Python Program For Stock Buy Sell To Maximize Profit
```python
def max_profit(prices, days):
    profit = 0
 
    for i in range(1, days):
 
        # Checks if elements are adjacent
        # and in increasing order
        if prices[i] > prices[i-1]:
 
            # Difference added to 'profit'
            profit += prices[i] - prices[i-1]
 
    return profit
```
Time Complexity: O(n)
Auxiliary Space: O(1)

#### Python program to print Pascal’s Triangle

Input: N = 5
Output:
```math
      1
     1 1
    1 2 1
   1 3 3 1
  1 4 6 4 1
```
```python
# input n
n = 5
 
for i in range(1, n+1):
    for j in range(0, n-i+1):
        print(' ', end='')
 
    # first element is always 1
    C = 1
    for j in range(1, i+1):
 
        # first value in a line is always 1
        print(' ', C, sep='', end='')
 
        # using Binomial Coefficient
        C = C * (i - j) // j
    print()
```
Time complexity: O(N2)

Or

11**0 = 1
11**1 = 11
11**2 = 121
11**3 = 1331
```python
# input n
n = 5
 
# iterarte upto n
for i in range(n):
    # adjust space
    print(' '*(n-i), end='')
 
    # compute power of 11
    print(' '.join(map(str, str(11**i))))
```
Time Complexity: O(N)
Auxiliary Space: O(1)

This approach is applicable up to n=5 only.

#### Find the missing and repeating number

Input: arr[] = {3, 1, 3}
Output: Missing = 2, Repeating = 3
Explanation: In the array, 2 is missing and 3 occurs twice 
```python
def main():
     
    arr = [ 4, 3, 6, 2, 1, 1 ]
     
    numberMap = {}
     
    max = len(arr)
    for i in arr:
        if not i in numberMap:
            numberMap[i] = True
             
        else:
            print("Repeating =", i)
     
    for i in range(1, max + 1):
        if not i in numberMap:
            print("Missing =", i)
```
#### Search insert position of K in a sorted array

Input: arr[] = {1, 3, 5, 6}, K = 5
Output: 2
Explanation: Since 5 is found at index 2 as arr[2] = 5, the output is 2.

Input: arr[] = {1, 3, 5, 6}, K = 2
Output: 1
Explanation: Since 2 is not present in the array but can be inserted at index 1 to make the array sorted.
```python
def find_index(arr, n, B):
 
    # Lower and upper bounds
    start = 0
    end = n - 1
 
    # Traverse the search space
    while start<= end:
 
        mid =(start + end)//2
 
        if arr[mid] == K:
            return mid
 
        elif arr[mid] < K:
            start = mid + 1
        else:
            end = mid-1
 
    # Return the insert position
    return end + 1
```
Time Complexity: O(log N)
Auxiliary Space: O(1)

#### Find first and last positions of an element in a sorted array

Input : arr[] = {1, 3, 5, 5, 5, 5, 67, 123, 125}    
        x = 5
Output : First Occurrence = 2
         Last Occurrence = 5
```python
def findFirstAndLast(arr, n, x) :
    first = -1
    last = -1
    for i in range(0, n) :
        if (x != arr[i]) :
            continue
        if (first == -1) :
            first = i
        last = i
      
    if (first != -1) :
        print( "First Occurrence = ", first, 
               " \nLast Occurrence = ", last)
    else :
        print("Not Found")
```
Time Complexity: O(n) 
Auxiliary Space: O(1)

#### Count occurrences of an element in a list

Input: lst = [15, 6, 7, 10, 12, 20, 10, 28, 10], x = 10
Output: 3 
Explanation: 10 appears three times in given list.
```python
def countX(lst, x):
    count = 0
    for ele in lst:
        if (ele == x):
            count = count + 1
    return count
```
Or
```python
def countX(lst, x):
    return lst.count(x)
```
#### K-th Element of Two Sorted Arrays

Input : Array 1 - 2 3 6 7 9
        Array 2 - 1 4 8 10
        k = 5
Output : 6
Explanation: The final sorted array would be -
1, 2, 3, 4, 6, 7, 8, 9, 10
The 5th element of this array is 6.
```python
def kth(arr1, arr2, m, n, k):
 
    sorted1 = [0] * (m + n)
    i = 0
    j = 0
    d = 0
    while (i < m and j < n):
 
        if (arr1[i] < arr2[j]):
            sorted1[d] = arr1[i]
            i += 1
        else:
            sorted1[d] = arr2[j]
            j += 1
        d += 1
 
    while (i < m):
        sorted1[d] = arr1[i]
        d += 1
        i += 1
    while (j < n):
        sorted1[d] = arr2[j]
        d += 1
        j += 1
    return sorted1[k - 1]
```
Time Complexity: O(n) 
Auxiliary Space : O(m + n) 
```python
def find(A, B, m, n, k_req):   
    i, j, k = 0, 0, 0
 
    # Keep taking smaller of the current
    # elements of two sorted arrays and
    # keep incrementing k
    while i < len(A) and j < len(B):
        if A[i] < B[j]:
            k += 1
            if k == k_req:
                return A[i]
            i += 1
        else:
            k += 1
            if k == k_req:
                return B[j]       
            j += 1
 
    # If array B[] is completely traversed
    while i < len(A):
        k += 1
        if k == k_req:
                return A[i]
        i += 1
 
 
    # If array A[] is completely traversed
    while j < len(B):
        k += 1
        if k == k_req:
                return B[j]
        j += 1
```
Time Complexity: O(k) 
Auxiliary Space: O(1)

#### Median of two sorted arrays of different sizes

Input: ar1[] = {-5, 3, 6, 12, 15}
        ar2[] = {-12, -10, -6, -3, 4, 10}
Output : The median is 3.
Explanation : The merged array is :
        ar3[] = {-12, -10, -6, -5 , -3,
                 3, 4, 6, 10, 12, 15},
       So the median of the merged array is 3
```python
def getMedian(ar1, ar2, n, m) :
 
    i = 0 # Current index of input array ar1[]
    j = 0 # Current index of input array ar2[]
    m1, m2 = -1, -1 
    for count in range(((n + m) // 2) + 1) :
      if(i != n and j != m) :
        if ar1[i] > ar2[j] :
          m1 = ar2[j]
          j += 1
        else :
          m1 = ar1[i]
          i += 1           
      elif(i < n) :       
        m1 = ar1[i]
        i += 1       
           # for case when j<m,
      else :
        m1 = ar2[j]
        j += 1
       # return m1 if it's lengt odd else return (m1+m2)//2
    return m1 if (n + m) % 2 == 1 else (m1 + m2) // 2
```
Time Complexity: O(m + n). To merge both the arrays O(m+n) time is needed.
Auxiliary Space: O(1). No extra space is required.

#### Reverse words in a given String in Python

Input : str =" geeks quiz practice code"
Output : str = code practice quiz geeks
```python
# input string
string = "geeks quiz practice code"
# reversing words in a given string
s = string.split()[::-1]
l = []
for i in s:
    # apending reversed words to l
    l.append(i)
# printing reverse words
print(" ".join(l))
```
Time Complexity: O(n), where n is the length of the string
Auxiliary Space: O(n), where n is the length of the string

#### Program to Print Largest Even and Largest Odd Number in a List

Input: 1 3 5 8 6 10 
Output:
Largest even number is  10 
Largest odd number is  5
```python
def printmax(lis):
   
    # Using list comprehension storing
    # even and odd numbers as separate lists
    even = [x for x in lis if x % 2 == 0]
    odd = [x for x in lis if x % 2 == 1]
 
    # printing max numbers in corresponding lists
    print("Largest odd number is ", max(odd))
    print("Largest even number is ", max(even))
```
Or
```python
def largestEven(list):
        curr = -1
        for num in list:
            num = int(num)
            if(num % 2 == 0 and num > curr):
                curr = num
 
        print("Largest even number is ", curr)
 
    def largestOdd(list):
        currO = -1
        for num in list:
            num = int(num)
            if(num % 2 == 1 and num > currO):
                currO = num
 
        print("Largest odd number is ", currO)
```
#### Check if two given strings are isomorphic to each other

Input:  str1 = "aab", str2 = "xxy"
Output: True
'a' is mapped to 'x' and 'b' is mapped to 'y'.
```python
def isIsomorphic(s, t):
        return [s.find(i) for i in s] == [t.find(j) for j in t]
```
#### Check whether two strings are anagram of each other

An anagram of a string is another string that contains the same characters, only the order of characters can be different. For example, “abcd” and “dabc” are an anagram of each other.
```python
def isAnagram(s, t):
        d = {}
        for i in s:
            if i in d: d[i] += 1
            else: d[i] = 1
        for i in t:
            if i in d: d[i] -= 1
            else: return False
        for k, v in d.items(): 
            if v != 0: return False
        return True
```
#### Sort list elements by frequency
```python
ini_list = [1, 1, 2, 2, 2, 3, 3, 3, 3, 3, 5, 5, 5, 4, 4, 4, 4, 4, 4]
 
# printing initial ini_list
print ("initial list", str(ini_list))
 
# sorting on basis of frequency of elements
result = sorted(ini_list, key = ini_list.count,
                                reverse = True)
 
# printing final result
print("final list", str(result))
```
Op:

initial list [1, 1, 2, 2, 2, 3, 3, 3, 3, 3, 5, 5, 5, 4, 4, 4, 4, 4, 4]
final list [4, 4, 4, 4, 4, 4, 3, 3, 3, 3, 3, 2, 2, 2, 5, 5, 5, 1, 1]

#### Program For Converting Roman Numerals To Decimal

Input: IX
Output: 9
IX is a Roman symbol which represents 9 
```python
def romanToInt(s):
        translations = {
            "I": 1,
            "V": 5,
            "X": 10,
            "L": 50,
            "C": 100,
            "D": 500,
            "M": 1000
        }
        number = 0
        s = s.replace("IV", "IIII").replace("IX", "VIIII")
        s = s.replace("XL", "XXXX").replace("XC", "LXXXX")
        s = s.replace("CD", "CCCC").replace("CM", "DCCCC")
        for char in s:
            number += translations[char]
        return number
```
#### String to Integer (atoi)

Input: s = "4193 with words"
Output: 4193
```python
def myAtoi(s):
        if not s: return 0
        n = len(s); i = 0; res = 0; flag = "+"
        while i<n and s[i]==" ": i+=1
        if i<n and (s[i] == "-" or s[i] == "+"):
            flag = s[i]
            i+=1
        while i<n:
            if s[i].isdigit():
                res = res*10 + int(s[i])
                i+=1    
            else: break
        res = res if flag == "+" else -res
        res = min(res, 2 ** 31 - 1)
        res = max(-(2 ** 31), res)
        return res
```
#### Write a program to calculate pow(x,n)

Input : x = 2, n = 3
Output : 8
```python
def power(x, y):
     
    # If x^0 return 1
    if (y == 0):
        return 1
     
    # If we need to find of 0^y
    if (x == 0):
        return 0
     
    # For all other cases
    return x * power(x, y - 1)
```
Time Complexity: O(n)
Auxiliary Space: O(n)

#### Program to print all prime factors of a given number

If the input number is 12, then the output should be “2 2 3”.
```python
def primeFactors(n):
 
    c = 2
    while(n > 1):
 
        if(n % c == 0):
            print(c, end=" ")
            n = n / c
        else:
            c = c + 1
 ```
Time Complexity: O(log n)
Auxiliary Space: O(1)

#### k largest(or smallest) elements in an array

If the given array is [1, 23, 12, 9, 30, 2, 50] and you are asked for the largest 3 elements i.e., k = 3 then your program should print 50, 30, and 23.
```python
def kLargest(arr, k):
    # Sort the given array arr in reverse
    # order.
    arr.sort(reverse = True)
    # Print the first kth largest elements
    for i in range(k):
        print (arr[i], end =" ")
```
Time complexity: O(n*log(n))
Auxiliary Space: O(1)

#### Replace each element of Array with it’s corresponding rank

Input: arr[] = [100, 5, 70, 2] 
Output: [4, 2, 3, 1] 
Explanation: 
Rank of 2 is 1, 5 is 2, 70 is 3 and 100 is 4.
```python
def changeArr(input1):
 
    # Copy input array into newArray
    newArray = input1.copy()
     
    # Sort newArray[] in ascending order
    newArray.sort()
     
    # Dictionary to store the rank of
    # the array element
    ranks = {}
     
    rank = 1
     
    for index in range(len(newArray)):
        element = newArray[index];
     
        # Update rank of element
        if element not in ranks:
            ranks[element] = rank
            rank += 1
         
    # Assign ranks to elements
    for index in range(len(input1)):
        element = input1[index]
        input1[index] = ranks[input1[index]]
```
Time Complexity: O(N * log N)
Auxiliary Space: O(N)

#### Tree Traversals (Inorder, Preorder and Postorder)
```python
# A function to do inorder tree traversal
def printInorder(root):
  
    if root:
  
        # First recur on left child
        printInorder(root.left)
  
        # then print the data of node
        print(root.val)
  
        # now recur on right child
        printInorder(root.right)  
```
```python
# A function to do postorder tree traversal
def printPostorder(root):
  
    if root:
  
        # First recur on left child
        printPostorder(root.left)
  
        # the recur on right child
        printPostorder(root.right)
  
        # now print the data of node
        print(root.val),
```
```python
# A function to do preorder tree traversal
def printPreorder(root):
  
    if root:
  
        # First print the data of node
        print(root.val),
  
        # Then recur on left child
        printPreorder(root.left)
  
        # Finally recur on right child
        printPreorder(root.right)
```
Time Complexity: O(n)
Auxiliary Space: O(1)

#### Level Order Binary Tree Traversal
```python
def printLevelOrder(root):
    # Base Case
    if root is None:
        return
 
    # Create an empty queue
    # for level order traversal
    queue = []
 
    # Enqueue Root and initialize height
    queue.append(root)
 
    while(len(queue) > 0):
 
        # Print front of queue and
        # remove it from queue
        print(queue[0].data)
        node = queue.pop(0)
 
        # Enqueue left child
        if node.left is not None:
            queue.append(node.left)
 
        # Enqueue right child
        if node.right is not None:
            queue.append(node.right)
```
Time Complexity: O(n) where n is the number of nodes in the binary tree.
Auxiliary Space: O(n) where n is the number of nodes in the binary tree.

#### Program to Find the Maximum Depth or Height of a Tree
```python
def maxDepth(node):
    if node is None:
        return -1 ;
 
    else :
 
        # Compute the depth of each subtree
        lDepth = maxDepth(node.left)
        rDepth = maxDepth(node.right)
 
        # Use the larger one
        if (lDepth > rDepth):
            return lDepth+1
        else:
            return rDepth+1
```
Time Complexity: O(n)
Auxiliary Space: O(n)

#### Check for Symmetric Binary Tree
```python
def isSymmetric(root):
    if not root:
        return True
    stack = [(root.left, root.right)]
    while stack:
        l, r = stack.pop()
        if not l and not r:
            continue
        if not l or not r:
            return False
        if l.val != r.val:
            return False
        stack.append((l.left, r.right))
        stack.append((l.right, r.left))
    return True
```

#### Search a node in Binary Tree
```python
def ifNodeExists(node, key):
 
    if (node == None):
        return False
 
    if (node.data == key):
        return True
 
    """ then recur on left subtree """
    res1 = ifNodeExists(node.left, key)
    # node found, no need to look further
    if res1:
        return True
 
    """ node is not found in left,
    so recur on right subtree """
    res2 = ifNodeExists(node.right, key)
 
    return res2
```
Time Complexity: O(N)
Auxiliary Space: O(N)

#### Find the node with minimum value in a Binary Search Tree
```python
def minValue(node):
    current = node
  
    # loop down to find the leftmost leaf
    while(current.left is not None):
        current = current.left
  
    return current.data
```
Time Complexity: O(N)
Auxiliary Space: O(N)

#### Program for Longest Common Subsequence
```python
def lcs(X, Y):
    # find the length of the strings
    m = len(X)
    n = len(Y)
 
    # declaring the array for storing the dp values
    L = [[None]*(n + 1) for i in range(m + 1)]
 
    """Following steps build L[m + 1][n + 1] in bottom up fashion
    Note: L[i][j] contains length of LCS of X[0..i-1]
    and Y[0..j-1]"""
    for i in range(m + 1):
        for j in range(n + 1):
            if i == 0 or j == 0 :
                L[i][j] = 0
            elif X[i-1] == Y[j-1]:
                L[i][j] = L[i-1][j-1]+1
            else:
                L[i][j] = max(L[i-1][j], L[i][j-1])
 
    # L[m][n] contains the length of LCS of X[0..n-1] & Y[0..m-1]
    return L[m][n]
```
Time Complexity: O(n*m)
Auxiliary Space: O(n*m)

#### Minimum Number of Platforms Required for a Railway/Bus Station

Input: arr[] = {9:00, 9:40, 9:50, 11:00, 15:00, 18:00}, dep[] = {9:10, 12:00, 11:20, 11:30, 19:00, 20:00} 
Output: 3 
Explanation: There are at-most three trains at a time (time between 9:40 to 12:00)
```python
def findPlatform(arr, dep, n):
   
    # plat_needed indicates number of platforms
    # needed at a time
    plat_needed = 1
    result = 1
 
    # run a nested loop to find overlap
    for i in range(n):
        # minimum platform needed
        plat_needed = 1
 
        for j in range(n):
            # check for overlap
            if i != j:
                if (arr[i] >= arr[j] and dep[j] >= arr[i]):
                    plat_needed += 1
 
        # update result
        result = max(result, plat_needed)
 
    return result
```
Time Complexity: O(n2)
Auxiliary space: O(1)

#### Stack in Python
```python
stack = []
 
# append() function to push
# element in the stack
stack.append('a')
stack.append('b')
stack.append('c')
 
print('Initial stack')
print(stack)
 
# pop() function to pop
# element from stack in
# LIFO order
print('\nElements popped from stack:')
print(stack.pop())
print(stack.pop())
print(stack.pop())
 
print('\nStack after elements are popped:')
print(stack)
```
Time Complexity: O(1)

#### Array implementation of queue
```python
# Initializing a queue
queue = []
  
# Adding elements to the queue
queue.append('a')
queue.append('b')
queue.append('c')
  
print("Initial queue")
print(queue)
  
# Removing elements from the queue
print("\nElements dequeued from queue")
print(queue.pop(0))
print(queue.pop(0))
print(queue.pop(0))
  
print("\nQueue after removing elements")
print(queue)
```
Time Complexity : O(1)

#### Print all subsequences of a string

Input : abc
Output : a, b, c, ab, bc, ac, abc
```python
def printSubsequence(input, output):
 
    # Base Case
    # if the input is empty print the output string
    if len(input) == 0:
        print(output, end=' ')
        return
 
    # output is passed with including the
    # 1st character of input string
    printSubsequence(input[1:], output+input[0])
 
    # output is passed without including the
    # 1st character of input string
    printSubsequence(input[1:], output)
```
#### Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```python
class Solution:
    def twoSum(self, nums, target):
        
    #     ls = len(nums)
    #     for i in range(ls):
    #         for j in range(i + 1, ls):
    #             if nums[i] + nums[j] == target:
    #                 return [i, j]
    
        hash_nums = {}
        for index, num in enumerate(nums):
            another = target - num
            try:
                hash_nums[another]
                return [hash_nums[another], index]
            except KeyError:
                hash_nums[num] = index
```
#### Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. The relative order of the elements should be kept the same.

Input: nums = [1,1,2]
Output: 2, nums = [1,2,_]
Explanation: Your function should return k = 2, with the first two elements of nums being 1 and 2 respectively.
It does not matter what you leave beyond the returned k (hence they are underscores).
```python
class Solution:
    def removeDuplicates(self, nums):
        if len(nums) == 0:
            return 0
        left = 0
        for i in range(1, len(nums)):
            if nums[left] == nums[i]:
                continue
            else:
                left += 1
                nums[left] = nums[i]
        return left + 1
```
#### Given an integer array nums and an integer val, remove all occurrences of val in nums in-place. The relative order of the elements may be changed.

Input: nums = [3,2,2,3], val = 3
Output: 2, nums = [2,2,_,_]
Explanation: Your function should return k = 2, with the first two elements of nums being 2.
It does not matter what you leave beyond the returned k (hence they are underscores).
```python
class Solution:
    def removeElement(self, nums, val):
        ls = len(nums)
        if ls == 0:
            return ls
        pos = 0
        for i in range(ls):
            if nums[i] == val:
                continue
            else:
                nums[pos] = nums[i]
                pos += 1
        return pos
```
#### Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

Input: nums = [1,3,5,6], target = 5
Output: 2
```python
class Solution:
    def searchInsert(self, nums, target):
        l, r = int(0), len(nums) - 1
        while l < r:
            mid = int((l + r) / 2)
            if nums[mid] < target:
                l = mid + 1
            else:
                r = mid
        if nums[l] < target:
            return l + 1
        return l     
```
#### You are given a large integer represented as an integer array digits, where each digits[i] is the ith digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading 0's.

Increment the large integer by one and return the resulting array of digits.

Input: digits = [1,2,3]
Output: [1,2,4]
Explanation: The array represents the integer 123.
Incrementing by one gives 123 + 1 = 124.
Thus, the result should be [1,2,4].
```python
class Solution:
    def plusOne(self, digits):
        ls = len(digits)
        for index in reversed(range(ls)):
            if digits[index] < 9:
                digits[index] += 1
                return digits
            else:
                digits[index] = 0
        digits.insert(0, 1)
        return digits
```
#### You are given two integer arrays nums1 and nums2, sorted in non-decreasing order, and two integers m and n, representing the number of elements in nums1 and nums2 respectively.

Merge nums1 and nums2 into a single array sorted in non-decreasing order.

Input: nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
Output: [1,2,2,3,5,6]
Explanation: The arrays we are merging are [1,2,3] and [2,5,6].
The result of the merge is [1,2,2,3,5,6] with the underlined elements coming from nums1.
```python
class Solution:
    def merge(self, nums1, m, nums2, n):
        p1, p2 = m - 1, n - 1
        pos = m + n - 1
        while p1 >= 0 and p2 >= 0:
            if nums1[p1] >= nums2[p2]:
                nums1[pos] = nums1[p1]
                p1 -= 1
            else:
                nums1[pos] = nums2[p2]
                p2 -= 1
            pos -= 1
        while p2 >= 0:
            nums1[pos] = nums2[p2]
            p2 -= 1
            pos -= 1
```
#### Given an integer array nums where the elements are sorted in ascending order, convert it to a height-balanced binary search tree.

A height-balanced binary tree is a binary tree in which the depth of the two subtrees of every node never differs by more than one.

Input: nums = [-10,-3,0,5,9]
Output: [0,-3,9,-10,null,5]
Explanation: [0,-10,5,null,-3,null,9] is also accepted:

![image](https://user-images.githubusercontent.com/97865583/192079233-0e687e78-369d-4df0-8676-b3dfc090cc71.png)

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right

class Solution:
    def sortedArrayToBST(self, nums):
        if not nums:
            return None
        mid = int(len(nums) / 2)
        root = TreeNode(nums[mid])
        root.left = self.sortedArrayToBST(nums[:mid])
        root.right = self.sortedArrayToBST(nums[mid + 1:])
        return root
```
#### Given an integer numRows, return the first numRows of Pascal's triangle.

In Pascal's triangle, each number is the sum of the two numbers directly above it.

Input: numRows = 5
Output: [[1],[1,1],[1,2,1],[1,3,3,1],[1,4,6,4,1]]
```python
class Solution:
    def generate(self, numRows):
        res = []
        for i in range(numRows):
            res.append([1])
            for j in range(1,i+1):
                if j == i:
                    res[i].append(1)
                else:
                    res[i].append(res[i-1][j-1]+res[i-1][j])
        return res
```
#### Given an integer rowIndex, return the rowIndexth (0-indexed) row of the Pascal's triangle.

Input: rowIndex = 3
Output: [1,3,3,1]
```python
class Solution:
    def getRow(self, rowIndex):
        res = []
        for i in range(rowIndex + 1):
            res.append([1])
            for j in range(1,i+1):
                if j == i:
                    res[i].append(1)
                else:
                    res[i].append(res[i-1][j-1]+res[i-1][j])
        return res[rowIndex]
```
#### You are given an array prices where prices[i] is the price of a given stock on the ith day.

You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock. Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
```python
class Solution:
    def maxProfit(self, prices):
        if len(prices) < 2:
            return 0
        min_price = prices[0]
        max_profit = 0
        for price in prices:
            if price < min_price:
                min_price = price
            if price - min_price > max_profit:
                max_profit = price - min_price
        return max_profit
```
#### Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

Input: nums = [2,2,1]
Output: 1
```python
class Solution:
    def singleNumber(self, nums):
        result = nums[0]
        for i in nums[1:]:
            result ^= i
        return result
```
#### Given an array nums of size n, return the majority element.

The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.

Input: nums = [3,2,3]
Output: 3
```python
class Solution:
    def majorityElement(self, nums):
        result = None
        count = 0
        for num in nums:
            if count == 0:
                result = num
            if result == num:
                count += 1
            else:
                count -= 1
        return result
```
#### Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

Input: nums = [1,2,3,1]
Output: true
```python
class Solution:
    def containsDuplicate(self, nums):
        return len(nums) != len(set(nums))
```
#### Given an integer array nums and an integer k, return true if there are two distinct indices i and j in the array such that nums[i] == nums[j] and abs(i - j) <= k.

Input: nums = [1,2,3,1], k = 3
Output: true
```python
class Solution:
    def containsNearbyDuplicate(self, nums, k):
        d = {}
        for i, n in enumerate(nums):
            if n in d and (i - d[n]) <= k:
                return True
            d[n] = i
        return False
```
#### Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array.

Input: nums = [3,0,1]
Output: 2
Explanation: n = 3 since there are 3 numbers, so all numbers are in the range [0,3]. 2 is the missing number in the range since it does not appear in nums.
```python
class Solution:
    def missingNumber(self, nums):
        nums_set = set(nums)
        n = len(nums) + 1
        for number in range(n):
            if number not in nums_set:
                return number
```
#### Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Input: nums = [0,1,0,3,12]
Output: [1,3,12,0,0]
```python
class Solution:
    def moveZeroes(self, nums):
        i = 0
        for j in range(len(nums)):
            if nums[j] != 0:
                nums[i], nums[j] = nums[j], nums[i]
                i += 1
```
#### Given two integer arrays nums1 and nums2, return an array of their intersection. Each element in the result must be unique and you may return the result in any order.

Input: nums1 = [1,2,2,1], nums2 = [2,2]
Output: [2]
```python
class Solution:
    def intersection(self, nums1, nums2):
        # return set(nums1) & set(nums2)
        
        visited, result = {}, []
        for num in nums1:
            visited[num] = num
        for num in nums2:
            if num in visited:
                result.append(num)
                visited.pop(num)
        return result
```
#### Given two integer arrays nums1 and nums2, return an array of their intersection. Each element in the result must appear as many times as it shows in both arrays and you may return the result in any order.

Input: nums1 = [1,2,2,1], nums2 = [2,2]
Output: [2,2]
```python
class Solution:
    def intersect(self, nums1, nums2):
        nums1.sort()
        nums2.sort()
        ans = []
        p1 = p2 = 0
        while p1 < len(nums1) and p2 < len(nums2):
            if nums1[p1] == nums2[p2]:
                ans.append(nums1[p1])
                p1 += 1
                p2 += 1
            elif nums1[p1] < nums2[p2]:
                p1 += 1
            else:
                p2 += 1
        return ans
```
#### Given an integer array nums, return the third distinct maximum number in this array. If the third maximum does not exist, return the maximum number.

Input: nums = [3,2,1]
Output: 1
Explanation:
The first distinct maximum is 3.
The second distinct maximum is 2.
The third distinct maximum is 1.
```python
class Solution:
    def thirdMax(self, nums):
        if nums is None:
            return
        
        n = list(set(nums))
        if len(n)<3:
            return max(n)
        else:
            return sorted(n)[-3]
```
#### Given an array nums of n integers where nums[i] is in the range [1, n], return an array of all the integers in the range [1, n] that do not appear in nums.

Input: nums = [4,3,2,7,8,2,3,1]
Output: [5,6]
```python
class Solution:
    def findDisappearedNumbers(self, nums):
        length_nums = len(nums)
        all_numbers_set = set(range(1, length_nums + 1))

        for num in nums:
            if num in all_numbers_set:
                all_numbers_set.remove(num)

        return list(all_numbers_set)
```
#### Given a binary array nums, return the maximum number of consecutive 1's in the array.

Input: nums = [1,1,0,1,1,1]
Output: 3
Explanation: The first two digits or the last three digits are consecutive 1s. The maximum number of consecutive 1s is 3.
```python
class Solution:
    def findMaxConsecutiveOnes(self, nums):
        nums.append(0)
        currentLength = 0
        maxLength = 0
        for i in nums:
            if i == 1:
                currentLength += 1
            else:
                if currentLength > maxLength:
                    maxLength = currentLength
                currentLength = 0
        return maxLength
```
#### Given an integer array nums, find three numbers whose product is maximum and return the maximum product.

Input: nums = [1,2,3,4]
Output: 24
```python
class Solution:
    def maximumProduct(self, nums):
        if len(nums) <= 3:
            product = 1
            
            for num in nums:
                product *= num
                
        
        nums = sorted(nums)
        
        return max(nums[0] * nums[1] * nums[2], nums[-3] * nums[-2] * nums[-1], nums[0] * nums[1] * nums[-1])
```
#### Given an integer array nums, return all the triplets [nums[i], nums[j], nums[k]] such that i != j, i != k, and j != k, and nums[i] + nums[j] + nums[k] == 0.

Input: nums = [-1,0,1,2,-1,-4]
Output: [[-1,-1,2],[-1,0,1]]
Explanation: 
nums[0] + nums[1] + nums[2] = (-1) + 0 + 1 = 0.
nums[1] + nums[2] + nums[4] = 0 + 1 + (-1) = 0.
nums[0] + nums[3] + nums[4] = (-1) + 2 + (-1) = 0.
The distinct triplets are [-1,0,1] and [-1,-1,2].
Notice that the order of the output and the order of the triplets does not matter.
```python
class Solution:
    def threeSum(self, nums):
        nums.sort()
        arr = []
        for i in range(len(nums)):
            l = i+1
            r = len(nums)-1
            while l < r:    
                if nums[l]+nums[r] + nums[i] == 0:
                    a =[nums[i],nums[l],nums[r]]
                    if a not in arr:
                        arr.append(a)
                    l+=1
                elif nums[l] + nums[r] + nums[i] > 0:
                    r-=1
                else:
                    l+=1
        return arr
```
#### Given an integer array nums of length n and an integer target, find three integers in nums such that the sum is closest to target. Return the sum of the three integers.

Input: nums = [-1,2,1,-4], target = 1
Output: 2
Explanation: The sum that is closest to the target is 2. (-1 + 2 + 1 = 2).
```python
class Solution:
    def threeSumClosest(self, nums, target):
        nums.sort() 
        n = len(nums)
        closestSum = sys.maxsize 
        for i in range(n-2):
            j,k = i+1,n-1 
            while j<k:
                sum = nums[i]+nums[j]+nums[k] 
                if (abs(target-closestSum) > abs(target-sum)):
                    closestSum = sum 
                if sum > target:
                    k-=1 
                else:
                    j+=1
        return closestSum
```
#### Given an array nums of n integers, return an array of all the unique quadruplets [nums[a], nums[b], nums[c], nums[d]] such that:

0 <= a, b, c, d < n
a, b, c, and d are distinct.
nums[a] + nums[b] + nums[c] + nums[d] == target

You may return the answer in any order.

Input: nums = [1,0,-1,0,-2,2], target = 0
Output: [[-2,-1,1,2],[-2,0,0,2],[-1,0,0,1]]
```python
class Solution:
    def fourSum(self, nums, target):
        nums.sort()
        arr = []
        for i in range(len(nums)):
            for j in range(i+1,len(nums)):
                l = j+1
                r = len(nums)-1
                while l < r:
                    if nums[l] + nums[r] + nums[i] + nums[j] == target :
                        a = [nums[i],nums[j],nums[l],nums[r]]
                        if a not in arr:
                            arr.append(a)
                            l+=1
                        else:
                            l+=1
                    elif nums[l] + nums[r] + nums[i] + nums[j] > target:
                        r-=1
                    else:
                        l+=1    
        return arr
```
#### Given an array of integers nums sorted in non-decreasing order, find the starting and ending position of a given target value. If target is not found in the array, return [-1, -1].

Input: nums = [5,7,7,8,8,10], target = 8
Output: [3,4]
```python
class Solution:
    def searchRange(self, nums, target):
        if target not in nums:
            return [-1,-1]
        result = []
        for i in range(len(nums)):
            if nums[i] == target:
                result.append(i)
                break
        for j in range(len(nums)-1, -1, -1):
            if nums[j] == target:
                result.append(j)
                break
        return result
```
#### Given an array nums of distinct integers, return all the possible permutations. You can return the answer in any order.

Input: nums = [1,2,3]
Output: [[1,2,3],[1,3,2],[2,1,3],[2,3,1],[3,1,2],[3,2,1]]
```python
class Solution:
    def permute(self, nums: List[int]) -> List[List[int]]:
        # return list(itertools.permutations(nums))
        
        if nums==[]:
            return [[]]
        res=[]
        for i in range(len(nums)):
            m=self.permute(nums[:i]+nums[i+1:])
            for k in m:
                res.append([nums[i]]+k)
        return res
```
#### Given an integer array nums, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

A subarray is a contiguous part of an array.

Input: nums = [-2,1,-3,4,-1,2,1,-5,4]
Output: 6
Explanation: [4,-1,2,1] has the largest sum = 6.
```python
class Solution:
    def maxSubArray(self, nums):
        cursum = 0
        maxsum = nums[0]
        for i in range(len(nums)):
            cursum += nums[i]
            if cursum > maxsum:
                maxsum = cursum
            if cursum < 0:
                cursum = 0
        return maxsum
```
#### Given an unsorted array of integers nums, return the length of the longest consecutive elements sequence.

Input: nums = [100,4,200,1,3,2]
Output: 4
Explanation: The longest consecutive elements sequence is [1, 2, 3, 4]. Therefore its length is 4.
```python
class Solution:
    def longestConsecutive(self, nums):
        nums = set(nums)
        max_count = 0
        for elem in nums:
            if elem - 1 not in nums:
                length = 0
                while elem in nums:
                    elem = elem+1
                    length+=1
                max_count = max(max_count, length)
        return max_count
```
#### Given an integer array nums, find a contiguous non-empty subarray within the array that has the largest product, and return the product.

The test cases are generated so that the answer will fit in a 32-bit integer.

Input: nums = [2,3,-2,4]
Output: 6
Explanation: [2,3] has the largest product 6.
```python
class Solution:
    def maxProduct(self, nums):
        curmin, curmax = 1, 1
        res = max(nums)
        for i in nums:
            if i == 0:
                curmin, curmax = 1, 1
                continue
            temp = curmax * i
            curmax = max(temp, curmin*i, i)
            curmin = min(temp, curmin*i, i)
            res = max(res, curmax)
        return res
```
#### Given a 1-indexed array of integers numbers that is already sorted in non-decreasing order, find two numbers such that they add up to a specific target number.

Let these two numbers be numbers[index1] and numbers[index2] where 1 <= index1 < index2 <= numbers.length. Return the indices of the two numbers, index1 and index2, added by one as an integer array [index1, index2] of length 2.

Input: numbers = [2,7,11,15], target = 9
Output: [1,2]
Explanation: The sum of 2 and 7 is 9. Therefore, index1 = 1, index2 = 2. We return [1, 2].
```python
class Solution:
    def twoSum(self, numbers, target):
        i, j = 0, len(numbers)-1
        while i < j:
            s = numbers[i] + numbers[j]
            if s == target:
                return [i+1, j+1]
            elif s > target:
                j -= 1
            else:
                i += 1
```
#### Given an integer n, return the number of prime numbers that are strictly less than n.

Input: n = 10
Output: 4
Explanation: There are 4 prime numbers less than 10, they are 2, 3, 5, 7.
```python
class Solution:
    def countPrimes(self, n):
        arr = [True for i in range(n)]
        if n == 0 or n==1:
            return 0
        arr[0] =  False
        arr[1] =  False
        for i in range(2,int(math.sqrt(n))+1):
            if arr[i] == True:
                for j in range(i*i,n,i):
                    arr[j] = False
        ct = [i for i in arr if i == True]
        return len(ct)
```
#### Given an integer array nums and an integer k, return the kth largest element in the array.

Note that it is the kth largest element in the sorted order, not the kth distinct element.

Input: nums = [3,2,1,5,6,4], k = 2
Output: 5
```python
class Solution:
    def findKthLargest(self, nums, k):
        # nums.sort()
        # return nums[len(nums)-k]
        
        if not nums:
            return 0
        heap = []
        for i in nums:
            heapq.heappush(heap, i)
            if len(heap) > k:
                heapq.heappop(heap)
        return heapq.heappop(heap)
```
#### Given an array of integers nums containing n + 1 integers where each integer is in the range [1, n] inclusive.

There is only one repeated number in nums, return this repeated number. You must solve the problem without modifying the array nums and uses only constant extra space.

Input: nums = [1,3,4,2,2]
Output: 2
```python
class Solution:
    def findDuplicate(self, nums):
        unique = set(nums)
        return (sum(nums)-sum(unique))//(len(nums)-len(unique))
        
        # left,right = 1, len(nums)-1
        # while left < right:
        #     mid = left + (right - left)//2
        #     count = 0
        #     for i in nums:
        #         if i <= mid:
        #             count+=1
        #     if count <= mid:
        #         left = mid + 1
        #     else:
        #         right = mid
        # return left
```
#### Given an integer array nums and an integer k, return the k most frequent elements. You may return the answer in any order.

Input: nums = [1,1,1,2,2,3], k = 2
Output: [1,2]
```python
class Solution:
    def topKFrequent(self, nums, k):
        uMap = {}
        res = []
        for i in nums:
            if i in uMap:
                uMap[i] += 1
            else:
                uMap[i] = 1
        
        res = sorted(uMap, key=uMap.get, reverse=True)
        return res[:k]
```
#### Given an integer array nums of length n where all the integers of nums are in the range [1, n] and each integer appears once or twice, return an array of all the integers that appears twice.

Input: nums = [4,3,2,7,8,2,3,1]
Output: [2,3]
```python
class Solution:
    def findDuplicates(self, nums):
        dictions = {} 
        for x in nums:
            if x in dictions:
                dictions[x] += 1
            else:
                dictions[x] = 1 
        returnList = [] 
        for key, values in dictions.items():
            if values >= 2:
                returnList.append(key)
        return returnList
```
#### Write a function to find the longest common prefix string amongst an array of strings. If there is no common prefix, return an empty string "".

Input: strs = ["flower","flow","flight"]
Output: "fl"
```python
class Solution:
    def longestCommonPrefix(self, strs):
        str1, str2 = min(strs), max(strs)
        i = 0
        while i < len(str1):
            if str1[i] != str2[i]:
                str1 = str1[:i]
            i +=1
        return str1
```
#### Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

An input string is valid if:
Open brackets must be closed by the same type of brackets.
Open brackets must be closed in the correct order.
Every close bracket has a corresponding open bracket of the same type.

Input: s = "()"
Output: true
```python
class Solution:
    def isValid(self, s):
        while len(s) > 0:
            l = len(s)
            s = s.replace('()','').replace('{}','').replace('[]','')
            if l==len(s): return False
        return True
```
#### Given two strings needle and haystack, return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

Input: haystack = "sadbutsad", needle = "sad"
Output: 0
Explanation: "sad" occurs at index 0 and 6.
The first occurrence is at index 0, so we return 0.
```python
class Solution:
    def strStr(self, haystack, needle):
        for i in range(0, len(haystack) - len(needle) + 1):
            if haystack[i:i+len(needle)] == needle:
                return i
        return -1
```
#### Given a string s consisting of words and spaces, return the length of the last word in the string.

A word is a maximal substring consisting of non-space characters only.

Input: s = "Hello World"
Output: 5
Explanation: The last word is "World" with length 5.
```python
class Solution:
    def lengthOfLastWord(self, s):
        wordlist = s.split()
        if wordlist:
            return len(wordlist[-1])
        return 0
```
#### Given two binary strings a and b, return their sum as a binary string.

Input: a = "11", b = "1"
Output: "100"
```python
class Solution:
    def addBinary(self, a, b):
        return bin(eval('0b' + a) + eval('0b' + b))[2:]
```
#### Given a string s, return true if it is a palindrome, or false otherwise.

A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

Input: s = "A man, a plan, a canal: Panama"
Output: true
Explanation: "amanaplanacanalpanama" is a palindrome.
```python
class Solution:
    def isPalindrome(self, s):
        s = ''.join(e for e in s if e.isalnum()).lower()
        return s==s[::-1]
```
#### Given two strings s and t, determine if they are isomorphic.

Two strings s and t are isomorphic if the characters in s can be replaced to get t. All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character, but a character may map to itself.

Input: s = "egg", t = "add"
Output: true
```python
class Solution:
    def isIsomorphic(self, s, t):
        return [s.find(i) for i in s] == [t.find(j) for j in t]
```
#### Given two strings s and t, return true if t is an anagram of s, and false otherwise.

An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.

Input: s = "anagram", t = "nagaram"
Output: true
```python
class Solution:
    def isAnagram(self, s, t):
        d = {}
        for i in s:
            if i in d: d[i] += 1
            else: d[i] = 1
        for i in t:
            if i in d: d[i] -= 1
            else: return False
        for k, v in d.items(): 
            if v != 0: return False
        return True
```
#### Write a function that reverses a string. The input string is given as an array of characters s.

You must do this by modifying the input array in-place with O(1) extra memory.

Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
```python
class Solution:
    def reverseString(self, s):
        s[:] = s[::-1]
```    
#### Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.

Input: s = "leetcode"
Output: 0
```python
class Solution:
    def firstUniqChar(self, s: str) -> int:
        d = {}
        for l in s:
            if l not in d: d[l] = 1
            else: d[l] += 1
        index = -1
        for i in range(len(s)):
            if d[s[i]] == 1:
                index = i
                break
        return index
```
#### You are given two strings s and t. String t is generated by random shuffling string s and then add one more letter at a random position. Return the letter that was added to t.

Input: s = "abcd", t = "abcde"
Output: "e"
Explanation: 'e' is the letter that was added.
```python
class Solution:
    def findTheDifference(self, s, t):
        for i in t:
            if s.count(i) != t.count(i):
                return i
```
#### Given two strings s and t, return true if s is a subsequence of t, or false otherwise.

A subsequence of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. (i.e., "ace" is a subsequence of "abcde" while "aec" is not).

Input: s = "abc", t = "ahbgdc"
Output: true
```python
class Solution:
    def isSubsequence(self, s, t):
        p1 = p2 = 0
        while p1 < len(s) and p2 < len(t):
            if s[p1] == t[p2]:
                p1 += 1
            p2 += 1
        return p1 == len(s)
```
#### Given two non-negative integers, num1 and num2 represented as string, return the sum of num1 and num2 as a string.

You must solve the problem without using any built-in library for handling large integers (such as BigInteger). You must also not convert the inputs to integers directly.

Input: num1 = "11", num2 = "123"
Output: "134"
```python
class Solution:
    def addStrings(self, num1, num2):
        def str_to_int(n):
            integer = {'0':0,'1':1,'2':2,'3':3,'4':4,'5':5,'6':6,'7':7,'8':8,'9':9}
            num = 0
            for i in n:
                num = num*10 + integer[i]
            return num
        res = str_to_int(num1)+str_to_int(num2)
        return str(res)
```
#### Given a string s, return the number of segments in the string.

A segment is defined to be a contiguous sequence of non-space characters.

Input: s = "Hello, my name is John"
Output: 5
Explanation: The five segments are ["Hello,", "my", "name", "is", "John"]
```python
class Solution:
    def countSegments(self, s):
        l= s.split()
        return len(l)
```
#### Given a string s, reverse the order of characters in each word within a sentence while still preserving whitespace and initial word order.

Input: s = "Let's take LeetCode contest"
Output: "s'teL ekat edoCteeL tsetnoc"
```pthon
class Solution:
    def reverseWords(self, s):
        split_list = s.split(" ")
        split_list = [i[::-1] for i in split_list]
        return " ".join(split_list)
```
#### Given a string s, return the string after replacing every uppercase letter with the same lowercase letter.

Input: s = "Hello"
Output: "hello"
```python
class Solution:
    def toLowerCase(self, s):
        r = ""
        for c in s:
            if "A" <= c <= "Z":
                r += chr(ord(c) - ord("A") + ord("a"))
            else:
                r += c
        return r
```
The ord() function returns the number representing the unicode code of a specified character.

#### Given an input string s, reverse the order of the words.

A word is defined as a sequence of non-space characters. The words in s will be separated by at least one space. Return a string of the words in reverse order concatenated by a single space.

Input: s = "the sky is blue"
Output: "blue is sky the"
```python
class Solution:
    def reverseWords(self, s):
        return " ".join(s.strip().split()[::-1])
```
#### Given a string s, remove duplicate letters so that every letter appears once and only once. You must make sure your result is the smallest in lexicographical order among all possible results.

Input: s = "bcabc"
Output: "abc"
```python
class Solution:
    def removeDuplicateLetters(self, s):
        stack=[]
        last_index={}
        for i,ch in enumerate(s):
            last_index[ch]=i
        for i,ch in enumerate(s):
            if ch in stack:
                continue
            while len(stack)!=0 and ch<stack[-1] and i<last_index[stack[-1]]:
                stack.pop()
            stack.append(ch)
        return "".join(stack)
```
#### Finding the Longest word in Python
```python
# list with words
>>> words_list = ["Python", "is", "very", "important", "language"]
# In max we will provide the listofwords and key=len as arguments 
>>> long_word = max(words_list, key=len)
>>> print(long_word)
```
#### Climbing Stairs using Python

In the climbing stairs problem, we need to count all the possible combinations to reach the top of a staircase. As it has a constraint, we can only climb one step or two steps at a time, so we have a choice of stepping on or skipping a step.
```python
def climbStairs(num):
    a = 1
    b = 1
    n = num - 1
    for i in range(n):
        c = a
        a = a + b
        b = c
```
#### Square Root using Python
```python
def mySqrt(x):
    left = 1
    right = x
    mid = 0
    while (left <= right):
        mid = (left + right) // 2
        if mid * mid == x:
            return mid
        elif mid * mid > x:
            right = mid - 1
        else:
            left = mid + 1
            sqrt
```
#### Group Elements of Same Indices using Python

To group elements of the same index, you will initially have two or more lists inside a list like [[a, b], [c, d]]. To group the elements of these lists, you need to create two new lists where you will store the elements of both the lists at index 0 [a, c] and index 1 [b, d].
```python
inputLists = [[10, 20, 30], [40, 50, 60], [70, 80, 90]]
outputLists = []
index = 0

for i in range(len(inputLists[0])):
    outputLists.append([])
    for j in range(len(inputLists)):
        outputLists[index].append(inputLists[j][ index])
    index = index + 1
a, b, c = outputLists[0], outputLists[1], outputLists[2]
print(a, b, c)
```
#### Calculating Execution Time of a Python Program
```python
from time import time
start = time()
# Your Python program
end = time()
execution_time = end - start
```
#### Python Program to Count Most Frequent Words in a File

Here you will be given a file, and you will be asked to find the most frequent words in that file along with the number of times they are present.
```python
words = []
with open("demofile.txt", "r") as f:
    for line in f:
        words.extend(line.split())

from collections import Counter
counts = Counter(words)
top5 = counts.most_common(5)
print(top5)
```
#### Python Program to Count Capital Letters in a File

You will be given a text file, and you will be asked to read the file without using a Python library and print the number of capital or lowercase letters in the text file.
```python
with open("text.txt") as file:
    count = 0
    text = file.read()
    for i in text:
        if i.isupper():
            count += 1
    print(count)
```
#### Python Program to Count Small Letters in a File
```python
with open("text.txt") as file:
    count = 0
    text = file.read()
    for i in text:
        if i.islower():
            count += 1
    print(count)
```
#### Index of the Maximum Value in a Python List
```python
def maximum(x):
    maximum_index = 0
    current_index = 1
    while current_index < len(x):
        if x[current_index] > x[maximum_index]:
            maximum_index = current_index
        current_index = current_index + 1
    return maximum_index
```
#### Index of Minimum Value in a Python List
```python
def minimum(x):
    minimum_index = 0
    current_index = 1
    while current_index < len(x):
        if x[current_index] < x[minimum_index]:
            minimum_index = current_index
        current_index = current_index + 1
    return minimum_index
```
#### Mean Median and Mode using Python
```python
# Mean
list1 = [12, 16, 20, 20, 12, 30, 25, 23, 24, 20]
mean = sum(list1)/len(list1)
print(mean)
```
```python
# Median
list1 = [12, 16, 20, 20, 12, 30, 25, 23, 24, 20]
list1.sort()

if len(list1) % 2 == 0:
    m1 = list1[len(list1)//2]
    m2 = list1[len(list1)//2 - 1]
    median = (m1 + m2)/2
else:
    median = list1[len(list1)
```
```python
# Mode
list1 = [12, 16, 20, 20, 12, 30, 25, 23, 24, 20]
frequency = {}
for i in list1:
    frequency.setdefault(i, 0)
    frequency[i]+=1

frequent = max(frequency.values())
for i, j in frequency.items():
    if j == frequent:
        mode = i
print(mode)
```
