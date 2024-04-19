# POTD-19-04-2024
Find missing in second array

class Solution
{
    ArrayList<Integer> findMissing(int a[], int b[], int n, int m)
    {
        HashSet<Integer> bSet = new HashSet<>();
        for (int num : b) {
            bSet.add(num);
        }
        
        ArrayList<Integer> missingNumbers = new ArrayList<>();
        for (int num : a) {
            // Check if the element from array a is not in array b
            if (!bSet.contains(num)) {
                missingNumbers.add(num);
            }
        }
        return missingNumbers;
    }
}

Input: 
n = 6, m = 5
a[] = {1, 2, 3, 4, 5, 10}
b[] = {2, 3, 1, 0, 5}
Output: 
4 10
