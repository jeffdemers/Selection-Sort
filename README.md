# Selection-Sort

The Gist

Selection sort is the most conceptually simple of all the sorting algorithms. It works by selecting the smallest (or largest, if you want to sort from big to small) element of the array and placing it at the head of the array. Then the process is repeated for the remainder of the array; the next largest element is selected and put into the next slot, and so on down the line.

Real-World Analogue

Sorting people by height. Take the first person and adding them to the front of the line. Repeat the process with the remaining people in the group.  Keep on repeating checking for shortest person until everyone in in the sorted group.

Is it good?

It's expensive the bigger the array the longer the process to iterate each time.  

Ruby Sample

<pre class="ruby">
def selectionsort(list)
 list.size.times do |start|
   min = start
   start.upto(list.size-1) do |i|
     min = i if list[i] < list[min]
   end
   list[start], list[min] = list[min], list[start]
 end
 list
end
</pre>
    
