class Solution {
    public long largestPerimeter(int[] nums) {
        Arrays.sort(nums);
        long[] prefixSum = new long[nums.length];
        prefixSum[0] = nums[0];
        for (int i = 1; i < prefixSum.length; i++) {
            prefixSum[i] = nums[i] + prefixSum[i - 1];
        }
        long result = Integer.MIN_VALUE;
        for (int i = 2; i < nums.length; i++) {
            if (nums[i] < prefixSum[i - 1]) {
                result = prefixSum[i];
            }
        }
        return (result == Integer.MIN_VALUE) ? -1 : result;
    }
}
