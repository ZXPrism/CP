# [CF25A](https://mirror.codeforces.com/problemset/problem/25/A)

## Tag
- `brute force`

## Solution
扫描一遍数组，找出奇数或偶数的个数，从而确定目标的奇偶性，然后再扫描一遍数组，找到目标。

## Code ($\mathcal{O}(n)$)
```cpp
void solve() {
    int n = 0;
    std::cin >> n;
    std::vector<int> v(n);
    for (int i = 0; i < n; i++) {
        std::cin >> v[i];
    }

    int odd = 0;
    for (int i = 0; i < n; i++) {
        odd += v[i] % 2;
    }
    int target = (odd == 1 ? 1 : 0);

    for (int i = 0; i < n; i++) {
        if (v[i] % 2 == target) {
            std::cout << i + 1 << '\n';
            return;
        }
    }
}
```
