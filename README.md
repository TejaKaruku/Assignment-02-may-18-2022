# Assignment-02-may-18-2022
l=list(map(int,input().split()))
n=len(l)
k=int(input())
count=0 
d={}
cur_sum=0
for i in range(n):
    cur_sum=cur_sum+l[i]
    if cur_sum==k:
        count=count+1
    if cur_sum-k in d:
        count=count+d[cur_sum]
    if cur_sum in d:
        d[cur_sum]=d[cur_sum]+1
    else:
        d[cur_sum]=1
print(count)
