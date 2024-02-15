# Programming-Assignment
Structify-Take Home Submission

Big O: O(n^2)
    
    starts = []
    ends = []
    for i in range(len(radians)):
        if radians[i]<6.28 and radians[i]>0:
            if 's' in identifiers[i]:
                starts.append([radians[i],identifiers[i]])
            else:
                ends.append([radians[i],identifiers[i]])
                
    starts.sort(key=lambda x: (x, x))
    ends.sort(key=lambda x: (x, x))
    intersections = 0
    
    for i in range(0,len(starts)):
        if i!=len(starts)-1:
            if ends[i][0]>starts[i+1][0]>starts[i][0] and ends[i+1][0]>ends[i][0]:
                intersections +=1

