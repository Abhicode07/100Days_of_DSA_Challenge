class Solution {
    public int findKthLargest(int[] nums, int k) {
        quickSelect(nums, 0, nums.length - 1, k - 1);
        return nums[k - 1];
    }

    Random r = new Random();
    private int[] pivot(int[] nums, int start, int end) {
        int idx = start + r.nextInt(end - start + 1);
        int pivoted = nums[idx];
        int i = start, j = start, k = end;
        while (j <= k) {
            if (nums[j] > pivoted) {
                swap(nums, i, j);
                i++;
                j++;
            } else if (nums[j] == pivoted) {
                j++;
            } else {
                swap(nums, j, k);
                k--;
            }
        }
        return new int[]{i, j};
    }

    private void swap(int[] nums, int i, int j) {
        int temp = nums[i];
        nums[i] = nums[j];
        nums[j] = temp;
        return;
    }

    private void quickSelect(int[] nums, int start, int end, int k) {
        if (start > end) {
            return;
        }
        int[] pivotRes = pivot(nums, start, end);
        if (k >= pivotRes[0] && k < pivotRes[1]) {
            return;
        }
        if (k < pivotRes[0]) {
            quickSelect(nums, start, pivotRes[0] - 1, k);
        } else {
            quickSelect(nums, pivotRes[1], end, k);
        }
    }
}
