# Two Oldest Ages
## Description

The two oldest ages function/method needs to be completed. It should take an array of numbers as its argument and return the two highest numbers within the array. The returned value should be an array in the format [second oldest age,  oldest age].

The order of the numbers passed in could be any order. The array will always include at least 2 items. If there are two or more oldest age, then return both of them in array format.

For example (Input --> Output):

[1, 2, 10, 8] --> [8, 10]
[1, 5, 87, 45, 8, 8] --> [45, 87]
[1, 3, 10, 0]) --> [3, 10]


## Solution
    <solution>
    #include <vector>
    #include <array>
    #include <algorithm>
    std::array<int, 2> two_oldest_ages(std::vector<int> ages)
    {
        int size = ages.capacity();
        sort(ages.begin(), ages.end());
        
        return {ages[size-2], ages[size-1]};
    }

