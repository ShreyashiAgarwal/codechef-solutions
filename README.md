# codechef-solutions(beginner questions)
......................................................................................................................................#
1.Secret Recipe
......................................................................................................................................#
Chef and his competitor Kefa own two restaurants located at a straight road. The position of Chef's restaurant is X1, the position of Kefa's restaurant is X2.

Chef and Kefa found out at the same time that a bottle with a secret recipe is located on the road between their restaurants. The position of the bottle is X3.

The cooks immediately started to run to the bottle. Chef runs with speed V1, Kefa with speed V2.

Your task is to figure out who reaches the bottle first and gets the secret recipe (of course, it is possible that both cooks reach the bottle at the same time).
#...................................................................................................................................#
Input
The first line of the input contains a single integer T denoting the number of test cases. The description of T test cases follows.
The first and only line of each test case contains five space-separated integers X1, X2, X3, V1 and V2.
Output
For each test case, print a single line containing the string "Chef" if Chef reaches the bottle first, "Kefa" if Kefa reaches the bottle first or "Draw" if Chef and Kefa reach the bottle at the same time (without quotes).
#....................................................................................................................................#
Example- Input
3
1 3 2 1 2
1 5 2 1 2
1 5 3 2 2
Example- Output
Kefa
Chef
Draw

Example case 1. Chef and Kefa are on the same distance from the bottle, but Kefa has speed 2, while Chef has speed 1

SOLUTION-
T = int(input())
for i in range(T):
    li = [ int(x) for x in input().split()]
    X1 = li[0]
    X2 = li[1]
    X3 = li[2]
    V1 = li[3]
    V2 = li[4]
    distance_chef = X3-X1
    distance_kefa = X2-X3
    time_chef = distance_chef/V1
    time_kefa = distance_kefa/V2
    if(time_chef==time_kefa):
        print("Draw")
    elif(time_chef<time_kefa):
        print("Chef")
    else:
        print("Kefa")


#......................................................................................................................................#
2.Fancy quotes
#......................................................................................................................................

"I don't have any fancy quotes." - meowcode

Chef was reading some quotes by great people. Now, he is interested in classifying all the fancy quotes he knows. He thinks that all fancy quotes which contain the word "not" are Real Fancy; quotes that do not contain it are regularly fancy.

You are given some quotes. For each quote, you need to tell Chef if it is Real Fancy or just regularly fancy.

Input
The first line of the input contains a single integer T denoting the number of test cases. The description of T test cases follows.
The first and only line of each test case contains a single string S denoting a quote.

Output
For each test case, print a single line containing the string "Real Fancy" or "regularly fancy" (without quotes).

Constraints
1≤T≤50
1≤|S|≤100
each character of S is either a lowercase English letter or a space

Example Input
2
i do not have any fancy quotes
when nothing goes right go left

Example Output
Real Fancy
regularly fancy

Explanation
Example case 1: "i do not have any fancy quotes"
Example case 2: The word "not" does not appear in the given quote
#......................................................................................................................................#
SOLUTION- 
T = int(input())
for i in range(T):
    S = input()
    l = S.split(" ")
    if("not" in l):
        print("Real Fancy")
    else:
        print("regularly fancy")
        
        
 #......................................................................................................................................#
 3.Mahasena
#......................................................................................................................................#

Kattapa, as you all know was one of the greatest warriors of his time. The kingdom of Maahishmati had never lost a battle under him (as army-chief), and the reason for that was their really powerful army, also called as Mahasena.

Kattapa was known to be a very superstitious person. He believed that a soldier is "lucky" if the soldier is holding an even number of weapons, and "unlucky" otherwise. He considered the army as "READY FOR BATTLE" if the count of "lucky" soldiers is strictly greater than the count of "unlucky" soldiers, and "NOT READY" otherwise.

Given the number of weapons each soldier is holding, your task is to determine whether the army formed by all these soldiers is "READY FOR BATTLE" or "NOT READY".

Input
The first line of input consists of a single integer N denoting the number of soldiers. The second line of input consists of N space separated integers A1, A2, ..., AN, where Ai denotes the number of weapons that the ith soldier is holding.

Output
Generate one line output saying "READY FOR BATTLE", if the army satisfies the conditions that Kattapa requires or "NOT READY" otherwise (quotes for clarity)

Example 1
Input:
1
1

Output:
NOT READY

Example 3
Input:
4
11 12 13 14

Output:
NOT READY
#......................................................................................................................................#
SOLUTION- 
N = int(input())
arr = [int(x) for x in input().split()]
c_even = 0
c_odd = 0
for i in arr:
    if(i%2==0):
        c_even = c_even+1
    else:
        c_odd = c_odd+1
if(c_even>c_odd):
    print("READY FOR BATTLE")
else:
    print("NOT READY")
    
  #......................................................................................................................................#
  
#......................................................................................................................................#
    
