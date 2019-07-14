# arrayRuby
Array Methods

There are a number of other useful methods available for manipulating arrays.
Here are some of the most used ones: |
-------------------------------------|--------------------------------
array.length or array.size |returns the number of elements in array.
array.sort | returns a new array with the elements sorted
array.uniq | returns a new array with duplicate values removed from array.
array.uniq!| removes duplicates in place.
array.freeze | safeguards the array, preventing it from being modified.
array.include?(obj)| returns true if obj is present in array, false otherwise.
array.min | returns the element with the minimum value.
array.max | returns the element with the maximum value.


 to add "z" to the array, remove all duplicates, and output the number of its elements.

          arr = ["a", "b", "a"]
          arr  << "z"
          arr.uniq!
          puts arr.size

Up until this point in the course, we've been working with different types of data, and generally we've been using variables to store that data. Variables are great because we can take pieces of data that would otherwise be difficult to remember and keep track of and store them in a nice, named container.

But variables as we've seen them so far do have one short coming, and that's when it comes to storing large amounts of related data.

Many of the programs that you'll find the real world, and that we'll be writing in this course will deal with large amounts of data. It could be a list of names, an index of phone numbers, the answers to a test, or any number of collections of data like these.

When you have lots of data like this that's meant to be grouped together, you can't use normal variables to store it. If you did you would need to create hundreds or thousands of variables, and that's assuming that you even know how many pieces of data would be in the collection.

Luckily for us the problem of storing large amounts of data like this has been solved with something called an array.

An array is a container which acts a lot like the variables we've seen so far in this course, except they allow us to store more than one piece of data.
So if you wanted to keep track of a list of names or phone numbers in Ruby, instead of storing them in separate variables you could store them in one massive array!

Creating an array
Let's take a look at how to create an array in Ruby:

lucky_numbers = [4, 8, "fifteen", 16, 23, 42.0]
#       indexes  0  1       2      3   4   5
You'll notice that creating an array is very similar to creating a variable. In this case we're storing a list of numbers inside the array. Notice how they're all separated with commas. In this case we're populating the array with numbers right off the bat, but a lot of times in programs you'll start with an empty or half empty array and fill it up as the program executes.

Array indexes
You'll also notice that I've indicated the indexes of each element in the array. Just like strings, which assign indexes to each of their characters, arrays elements also have indexes.

We start with the first element at index position 0, the indexes then increment by one from there. Just like strings you have to get used to the first element being at index position 0. This is something that commonly trips up new programmers!

The array is an entity in itself, but if you want to access an element inside the array you can do so by referring to it directly by it's index. Let's take a look at accessing an element in an array:

lucky_numbers[0] = 90
puts lucky_numbers[0]
puts lucky_numbers[1]
puts lucky_numbers.length
The elements inside the array are just normal strings, numbers or booleans. So once you've accessed one they can be treated like you would normally treat one of those data types. You can also modify the elements in an array by simply assigning them a new value as you can see above.

Wrapping it up
So there you have it, an introduction to arrays! Take a look at the video above for more information and to get a full step by step walk through of working with arrays!

Video Code
Copy
lucky_numbers = [4, 8, "fifteen", 16, 23, 42.0]
#       indexes  0  1       2      3   4   5

lucky_numbers[0] = 90
puts lucky_numbers[0]
puts lucky_numbers[1]
puts lucky_numbers[-1]

puts "\n\n"
puts lucky_numbers[2,3]
puts "\n\n"
puts lucky_numbers[2..4]
puts "\n\n"

puts lucky_numbers.length

---------------------------------------

Adding Elements

An array can contain different types of elements:
arr = [5, "Dave", 15.88, false]

puts arr[0] # 5
puts arr[1] # "Dave"
puts arr[-1] # false


To add new elements to the array, you can use the << operator, which is typed as two less than signs:
arr << 8

puts arr


This will add an element with the value 8 to the end of the array.
Alternatively, you can use the push and insert methods (we will learn more about methods in the coming module. For now, just remember that a method is code that performs an action).
arr.push(8)


This will add 8 to the end of the array.

The insert method allows you to insert the element at the desired position:
arr.insert(2, 8)
