int maxLevelSum(struct TreeNode* root) {
    struct TreeNode* q[10001];
    int front = 0, rear = 0;
    q[rear++] = root;

    int level = 1, ans = 1;
    long long maxSum = -1000000000000000000LL;

    while (front < rear) {
        int size = rear - front;
        long long sum = 0;

        for (int i = 0; i < size; i++) {
            struct TreeNode* node = q[front++];
            sum += node->val;
            if (node->left) q[rear++] = node->left;
            if (node->right) q[rear++] = node->right;
        }

        if (sum > maxSum) {
            maxSum = sum;
            ans = level;
        }
        level++;
    }
    return ans;
}
