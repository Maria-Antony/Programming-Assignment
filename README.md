# Programming-Assignment
Structify-Take Home Submission
Big O: O(n^2)

def count_intersections(radians, identifiers):
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
                
    return intersections

##radians = [0.9,1.3,1.7,2.92]
##identifiers = ["s_1", "e_1", "s_2", "e_2"]
##result = count_intersections(radians, identifiers)
##print(result)

Big O: O(n^2)
