# Selection-Sort

# The Gist

Selection sort is the most conceptually simple of all the sorting algorithms. It works by selecting the smallest (or largest, if you want to sort from big to small) element of the array and placing it at the head of the array. Then the process is repeated for the remainder of the array; the next largest element is selected and put into the next slot, and so on down the line.

# Real-World Analogue

Sorting people by height. Take the first person and adding them to the front of the line. Repeat the process with the remaining people in the group.  Keep on repeating checking for shortest person until everyone in in the sorted group.

# Is it good?

The main advantage of the selection sort is that it performs well on a small list. Furthermore, because it is an in-place sorting algorithm, no additional temporary storage is required beyond what is needed to hold the original list. The primary disadvantage of the selection sort is its poor efficiency when dealing with a huge list of items.


# Ruby Sample

a = [9,8,6,1,2,5,4,3,9,50,12,11]
n = a.size - 1

n.times do |i|
 index_min = i

 (i + 1).upto(n) do |j|
   index_min = j if a[j] < a[index_min]
 end
 
 # Yep, in ruby I can do that, no aux variable. w00t!
 a[i], a[index_min] = a[index_min], a[i] if index_min != i
end
