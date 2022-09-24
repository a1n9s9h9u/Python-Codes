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
      1
     1 1
    1 2 1
   1 3 3 1
  1 4 6 4 1
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
#### 
