wk 4 - 1902
  
# 1 Sleepy Cow Herding 
  
  * insight: each move fills 1 hole
  *  max is easier: need find one [i, j] that contains maximum number of holes.
       * [0, N) -- any other range is contained inside [0, N)
          (A[N-1] - A[0] - 1) - (N-2) -> max
  *  min need direct at the final solution --> a range of N
       * find a [i, j) where A[j] - A[i] >= N-1
```
for i=0:N
    for j=i+1:N
        if (A[j] - A[i] >= N-1)
            ....  -> n
            break
    // update the new minimum             
    if min > n
       min = n
```    

```
    if (A[j] - A[i] == N-1) {
         n = (N-2) - (j-i-1)
    } else if (A[j] - A[i] > N-1) {
         n = (N-2) - (j-i-1) + 1
    }
```
* Obvious corner cases: 0 moves: A[N-1] - A[0] == N-1

# 2 Painting the Barn
* prefix sum algorithm

* Try the bronze first
```
/* Highly recommend to use multipl files */
foreach rect -> x1, x2, y1, y2
    for i=y1:y2+1
        for j=x1:x2+2
            grid[i][j]++
for i, j in grid
    if grid[i][j] == K
       count++  
print count
```
* Optimize
* 1-D prefix sum: grid[i] -> increment[i]

* Canonical form of prefix sum
```
// prepare input
foreach range -> x1, x2
    A[x1]++
    A[x2]--
// do moving sum                 
sum = 0                 
for x=0:N
    sum+=A[x]  --> instead, if you do `for i=0:x; sum++` , you recover the bronze method
    sum[i]==sum
```            

* from 1-D to 2-D ... to n-D
   * sometime is to do 2D corner
   * loop through 1 D and and do prefix sum on another D
   
# 3 Classical finding region problem -- back tracking

                 
