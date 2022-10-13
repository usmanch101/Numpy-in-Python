# Numpy-in-Python
NumPy is the fundamental package for scientific computing in Python. NumPy arrays have a fixed size at creation, unlike Python lists.

What is NumPy?
NumPy is a Python library used for working with arrays. It also has functions for working in domain of linear algebra, fourier transform, and matrices.
NumPy was created in 2005 by Travis Oliphant. It is an open source project and you can use it freely.NumPy stands for Numerical Python.
Why Use NumPy?
In Python we have lists that serve the purpose of arrays, but they are slow to process. NumPy aims to provide an array object that is up to 50x faster than traditional Python lists.
The array object in NumPy is called ndarray, it provides a lot of supporting functions that make working with ndarray very easy. Arrays are very frequently used in data science, where speed and resources are very important.


import numpy as np

# arange is used to define value within the limit
my_arr = np.arange(1,8)
my_arr = np.arange(1,8,2)
print(my_arr)
print(type(my_arr))


# arr to list
ar_lst = np.array([1,2,3,4])
print(ar_lst)


b = np.zeros((3,3))

b[1:] = 2
print(b)

a = np.arange(1,10).reshape((3,3))
print(a)
print(a.dtype)

s = a.sum()
f = a.sum(0)
f = a.sum(axis=1)
print(s)
print(f)

# array product 
array_product = a.prod()
print(array_product)


#taking mean (Average of the array)
array_average = a.mean()
print(array_average)

#maximum and Minimum value 

aray_max, aray_min =  a.max(), a.min()
print(aray_max, aray_min)

#arguments finding index

aray_max_ind, aray_min_ind = a.argmax(), a.argmin()
print(aray_max_ind, aray_min_ind)

#peak to peak method max()-min()
peak_to_peak = a.ptp()
print(peak_to_peak)

# size attribute is used to return the length of the array and total number of item and convert to one dimensional array 
array_size = a.reshape(a.size)
print(array_size)

#flatten method is create a copy of the origional array
array_flat = a.flatten()
print(array_flat)

# b ravel is to create the view the view of origional array
array_flat = a.ravel()
print(array_flat)

# repeat function just deal with repetation
array_repeat = np.repeat(a,3,axis=0)
print(array_repeat)

# unique function is opposite to repeat function
uniquw_aray = np.unique(array_repeat)
print(uniquw_aray)

# diagonal just sound fetch in the array
diagonal_aray = np.diagonal(a)
diagonal_aray = np.diagonal(a, offset = 1)
print(diagonal_aray)

# Conversion array to list
cvrt_list = a.tolist()
print("type of a is: ", type(cvrt_list))
print(cvrt_list)

# Swapping is use to swap the rows and column same as transpose
swap_arr = np.swapaxes(a,0,1)
print(swap_arr)


# Transpose is used to convert the colum into rows
Trans_arr = a.transpose(1,0)
print(Trans_arr)

# T method is used for transpose shortcut
Tras = a.T
print(Tras)

# Operation between two matrices multipliation, addition, substraction, division
x = [[1,2,3],
     [4,3,5]]
y = [[2,5,6],
     [5,7,3]]
w= np.add(x,y)  # addition method
print(w)

z = np.multiply(x,y) # multiplication method
print(z)

z = np.subtract(x,y) # substraction method
print(z)

z = z/y # floor divison
print(z)


# converstion to diagonal and changing values
eye_arr = np.eye(4)
print(eye_arr)
eye_arr = np.eye(4,k=1)
print(eye_arr)
eye_arr = np.eye(4,k=-1)
print(eye_arr) #diogonal

# Changing Array 

eye_arr[eye_arr == 0] =2
print(eye_arr)

eye_arr[eye_arr < 2] = 10
print(eye_arr)
