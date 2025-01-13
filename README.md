# Shazam-Clone
I am working on a project that takes the audio input and compares it with thousands of songs and identifies it. Just like Shazam does.

step1:
using a python library we will be able to record an audio file in mp3 format
step2:
we then convert this mp3 file into a spectogram
this spectogram is a 3d representation of the mp3 file w.r.t. amplitude time and frequency
step3:
using another library we then convert this graph into many small segments
step4:
we then mark down the highest and lowest amplitude points from this segment and all the other segments
NOTE: these highest and lowest amplitude points would be such that they make a huge diffrenece between the frequency chart in a plane.
example:  At a certain point where the frequency jumps from a very low valuse to a very hiigh value.
we will note down these point as KEY POINTS
step5:
when we save all the nodes of these KEY POINTS, we should end up with an array of all the key points.
Through this array we should also be able to map back to the original timeline of the spectogram.
step6:
now using both the spectogram and the array of KEY POINTS we will create another array that stores the descrete distances from (0,0) on the spectogram to all the KEY VALUES on the same graph.
we will call this the DISTANCE ARRAY.
step7:
This distance array will then be created into a single hash value.
This might not work properly so the more simplified step to work on it would be a linear search of every single point with reference to 0,0 on graph and then linearly adding a single point again and again to search. so to avoid failure in searching.
To save time we can change the approach from being linear to binary or ternary or other more simplified search algorithm.
and then convert the search data into hash functions, Since all the data we will be comparing our working sample with will be in the form of HASHES.


