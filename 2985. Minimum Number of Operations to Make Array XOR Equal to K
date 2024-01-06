class Solution {
    public int minOperations(int[] nums, int k) {
        int xor = nums[0];
        for (int i = 1; i < nums.length; i++) {
            xor ^= nums[i];
        }
        if (xor == k) {
            return 0;
        }
        return countOperations(xor, k);
    }
    public int countOperations(int x, int y){
        int diffBits = 0;
        for (int i = 0; i < 32; i++) {
            int xLSB = ((x >> i) & 1);
            int yLSB = ((y >> i) & 1);
            if (xLSB != yLSB) {
                diffBits++;
            }
        }
        return diffBits;
    }
}
