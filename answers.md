# CMPS 2200 Assignment 5                                                                                                                                                                
## Answers                                                                                                                                                                              
                                                                                                                                                                                        
**Name:**_________Joshua Sasson__________                                                                                                                                               
                                                                                                                                                                                        
                                                                                                                                                                                        
                                                                                                                                                                                        
                                                                                                                                                                                        
                                                                                                                                                                                        
                                                                                                                                                                                        
- **1a.**                                                                                                                                                                               
the max depth of a d-ary heap is logd(n) where d is the number of children each node has                                                                                                
and n is the number of nodes in the heap                                                                                                                                                
                                                                                                                                                                                        
- **1b.**                                                                                                                                                                               
The max depth is logd(n) for the d-ary heap                                                                                                                                             
The insert operation puts a node at the bottom right and swaps upward making one comparison at each level                                                                               
So the max work is 1 for each level and logd(n) levels so O(logd(n))                                                                                                                    
                                                                                                                                                                                        
The delete operation puts a node at the top and swaps downward making d comparisons at each level                                                                                       
So the max work is d for each level and logd(n) levels so O(dlogd(n))                                                                                                                   
                                                                                                                                                                                        
                                                                                                                                                                                        
- **1c.**                                                                                                                                                                               
Djistras algorthim steps:                                                                                                                                                               
1. pop/delete min node (happnes to all nodes V once work of V*dlogd(n) )                                                                                                                
2. add edge nodes to frontier (happens to all edges once work of E*logd(n))                                                                                                             
3. constant time work of updating a vistied list and adding up result                                                                                                                   
total W = V*dlogd(n) + E*logd(n) + c                                                                                                                                                    
O(V*dlogd(n) + E*logd(n))                                                                                                                                                               
                                                                                                                                                                                        
- **1d.**                                                                                                                                                                               
If we pick a d such that V*d= m then the two costs of deleting nodes and adding edges will be equal                                                                                     
2(E)logd(V)                                                                                                                                                                             
2(E)logE/V(V) = E(lg(V)/lg(E/V))                                                                                                                                                        
lg(V)/lg(E/V) = 1/e                                                                                                                                                                     
O(E/e)= O(E)                                                                                                                                                                            
                                                                                                                                                                                        
                                                                                                                                                                                        
- **2a.**                                                                                                                                                                               
APSP(0,1,0)=N/A                                                                                                                                                                         
APSP(0,1,1)= -2                                                                                                                                                                         
APSP(0,1,2)= -2                                                                                                                                                                         
                                                                                                                                                                                        
APSP(0,2,0)= N/A                                                                                                                                                                        
APSP(0,2,1)= 2                                                                                                                                                                          
APSP(0,2,2)= -1                                                                                                                                                                         
                                                                                                                                                                                        
APSP(1,0,0)= N/A                                                                                                                                                                        
APSP(1,0,1)= -2                                                                                                                                                                         
APSP(1,0,2)= -2                                                                                                                                                                         
                                                                                                                                                                                        
APSP(1,2,0)= N/A                                                                                                                                                                        
APSP(1,2,1)= 1                                                                                                                                                                          
APSP(1,2,2)= 0                                                                                                                                                                          
                                                                                                                                                                                        
APSP(2,0,0)= N/A                                                                                                                                                                        
APSP(2,0,1)= 2                                                                                                                                                                          
APSP(2,0,2)= -1                                                                                                                                                                         
                                                                                                                                                                                        
APSP(2,1,0)= N/A                                                                                                                                                                        
APSP(2,1,1)= 1                                                                                                                                                                          
APSP(2,1,2)= 0                                                                                                                                                                          
                                                                                                                                                                                        
APSP(0,0,0)= 0                                                                                                                                                                          
APSP(0,0,1) =0                                                                                                                                                                          
APSP(0,0,2)=0                                                                                                                                                                           
                                                                                                                                                                                        
APSP(1,1,0)= 0                                                                                                                                                                          
APSP(1,1,1) =0                                                                                                                                                                          
APSP(1,1,2) =0                                                                                                                                                                          
                                                                                                                                                                                        
APSP(2,2,0)=0                                                                                                                                                                           
APSP(2,2,1)=0                                                                                                                                                                           
APSP(2,2,2)=0                                                                                                                                                                           
                                                                                                                                                                                        
                                                                                                                                                                                        
- **2b.**                                                                                                                                                                               
No there is not necessairly see a pattern since sometimes adding a new node allowed does not reduce the shortest path                                                                   
and sometimes it does. In order to create a relationship we need to know if the new path will be shorter than the old                                                                   
path.                                                                                                                                                                                   
                                                                                                                                                                                        
                                                                                                                                                                                        
- **2c.**                                                                                                                                                                               
APSP(i,j,k) = min( APSP(i,j,k-1)), APSP(i,k,k-1)+ APSP(k,j,k-1)                                                                                                                         
                                                                                                                                                                                        
                                                                                                                                                                                        
- **2d.**                                                                                                                                                                               
for each APSP call the work is V so since we call it three times for each V the work is V*V*V                                                                                           
or O(|V|^3)                                                                                                                                                                             
                                                                                                                                                                                        
- **2e.**                                                                                                                                                                               
Johnson's Algorithm has work O(|V| * |E|log(|E|))                                                                                                                                       
if |E|log(|E|)> V^2 then we should use our algorithm                                                                                                                                    
                                                                                                                                                                                        
                                                                                                                                                                                        
                                                                                                                                                                                        
- **3a.**                                                                                                                                                                               
Yes, since it is a tree format. If the MST was not the MMET then there would be a shorter path choice at at least one point. This tree
would not be a MST.                         
                                                                                                                                                                                        
- **3b.**                                                                                                                                                                               
Start with the optimal soltuion swap an E out for all possible swaps storing the path value                                                                                             
then pick the lowest value from this set                                                                                                                                                
                                                                                                                                                                                        
                                                                                                                                                                                        
- **3c.**                                                                                                                                                                               
From notes MST work is |E|log(|E|)                                                                                                                                                      
Worst case is |E| swaps so |E|*|E|log(|E|) so O(|E|^2 log(|E|))                                                                                                                         
                                                                                                                                                                                        
