Han Academy USACO 2020 - Spring

Class notes

Homework

```
prob1_bronze.cpp
prob2_bronze.cpp
prob3_bronze.cpp
prob1_silver.cpp
prob2_silver.cpp
prob3_silver.cpp
```

prob1_bronze.cpp
```
// Name: Hui Zhou
// Tests: 1/10 5, 6, 7 Timeout, 2,3,4 fail
// Feedback: anything goes. but the goal is a self reflection

#include <stdio.h>
#include <algorithm.h>

int N, K;
int cow_list[100000];
int main() {
   // ---- input block ----
   File *In = fopen("mixmilk.in", "r");
   fscanf(In, "%d %d", &N, &K);
   for (int i=0;i<N;i++) {
       fscanf(In, "%d", &cow_list[i]);
   }    
   fclose(In);
   
   // ---- preprocessing block ---
   std::sort(cow_list, cow_list+N);
   
   // ---- algorithm block
   int ans = solve()
   
   // ---- output block
   File *Out = fopen("mixmilk.out", "w");
   fprintf(Out, "%d\n", ans);
   fclose(Out);
   
}

int solve(){
    ...
}
```
