# [CF4C](https://mirror.codeforces.com/problemset/problem/4/C)

## Tag
- `implementation`

## Solution
按题意模拟即可。

## Code ($\mathcal{O}(n)$)
```cpp
void solve() {
    int n = 0;
    std::cin >> n;
    std::unordered_map<std::string, int> cnt;
    for (int i = 0; i < n; i++) {
        std::string s;
        std::cin >> s;
        if (++cnt[s] == 1) {
            std::cout << "OK\n";
        } else {
            std::cout << s << cnt[s] - 1 << '\n';
        }
    }
}
```
