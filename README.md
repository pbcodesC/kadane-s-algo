# kadane-s-algo
 int maxSubArraySum(int arr[], int n) {
        int max_so_far = INT_MIN;
        int curr_max = 0;

        for (int i = 0; i < n; i++) {
            curr_max += arr[i];

            if (curr_max > max_so_far)
                max_so_far = curr_max;

            if (curr_max < 0)
                curr_max = 0;
        }

        return max_so_far;
    }
};
