Write a closed-form expression for the number of times `do_work()` is called in terms of $N$.

count = 0
for i = 1 to N do
    for j = 1 to i do
        do_work()
        count = count + 1
    end
end

Answer: ending each iteration of the outer loop, the inner loop runs i times, leading to a total of 1 + 2 + 3 + ... + N = N(N + 1)/2 iterations of do_work(). Therefore, the time complexity of this code is O(N^2).

If $N=16$, how many times is `do_work()` called?

i = N
while i > 0:
    for j = 1 to i:
        do_work()
    i = floor(i / 2)

Answer: 31, because the outer loop runs for i = 16, 8, 4, 2, 1, and the inner loop runs for j = 1 to i. The total number of calls to `do_work()` is:
- When i = 16: 16 calls
- When i = 8: 8 calls
- When i = 4: 4 calls
- When i = 2: 2 calls
- When i = 1: 1 call
Total: 16 + 8 + 4 + 2 + 1 = 31 calls