# Binary Search

* [#540-single-element-in-a-sorted-array-m](../by-number/500-550.md#540-single-element-in-a-sorted-array-m "mention")
*   [#875-koko-eating-bananas-m](../by-number/850-900.md#875-koko-eating-bananas-m "mention")

    [#1283-find-the-smallest-divisor-given-a-threshold-m](../by-number/1250-1300.md#1283-find-the-smallest-divisor-given-a-threshold-m "mention")

    [#1891-cutting-ribbons-m](../by-number/1850-1900.md#1891-cutting-ribbons-m "mention")
* [#240-search-a-2d-matrix-ii-m](../by-number/200-250.md#240-search-a-2d-matrix-ii-m "mention")
* [#410-split-array-largest-sum-h](../by-number/400-450.md#410-split-array-largest-sum-h "mention")
* [#441-arranging-coins-e](../by-number/400-450.md#441-arranging-coins-e "mention")
* [#493-reverse-pairs-h](../by-number/450-500.md#493-reverse-pairs-h "mention")
* [#378-largest-divisible-subset](../by-number/page-3.md#378-largest-divisible-subset "mention")
*   Sort first and then do a binary search

    [#826-most-profit-assigning-work-m](../by-number/800-850.md#826-most-profit-assigning-work-m "mention")&#x20;

    [#1498-number-of-subsequences-that-satisfy-the-given-sum-condition-m](../by-number/1450-1500.md#1498-number-of-subsequences-that-satisfy-the-given-sum-condition-m "mention")
* [#1060-missing-element-in-sorted-array-m](../by-number/1050-1100.md#1060-missing-element-in-sorted-array-m "mention")

```
nums = [3, 6, 6, 6, 6, 7, 9]
bisect_left(nums, 6)  # result will be 1
bisect_right(nums, 6) # result will be 4
```

## Boundary problem

1.  l < r or l <= r

    If `while l < r`:

    Then after the loop, l = r, will return the first value larger or equal to the target value&#x20;

    If `while l <= r` :

    Then after the loop, l > r, then l is the first value larger or equal to the target value, and r will be the last value less than the target value.
2.  `bisect_left` or `bisect_right`&#x20;

    These two are equal to each other when the value is not in the list.

    Biggest different will be when value is in the list and has duplicated value

    e.g.

    ```
    nums = [3, 6, 6, 6, 6, 7, 9]
    bisect_left(nums, 6)  # result will be 1
    bisect_right(nums, 6) # result will be 4
    ```
