Minimum Loss
Problem Statement

Lauren has a list of distinct house prices over several years. She must buy a house in one year and sell it in a later year at a lower price, resulting in a loss.

The objective is to find the minimum possible loss while ensuring that the purchase occurs before the sale.

Approach

To efficiently find the minimum loss:

Store each house price along with its original year index.
Sort the prices in ascending order.
Compare adjacent prices in the sorted list.
A valid transaction exists only if the higher price occurred earlier than the lower price.
Track the smallest valid price difference.

Since the minimum loss must occur between two close prices, checking only adjacent sorted prices is sufficient.

Algorithm
Create (price, year) pairs.
Sort the pairs by price.
Iterate through adjacent pairs:
Verify that the higher price was recorded before the lower price.
Calculate the loss.
Update the minimum loss if smaller.
Return the minimum loss.
Complexity Analysis
Time Complexity: O(n log n) (sorting)
Space Complexity: O(n)
Example
Input
5
20 7 8 2 5
Output
2
Explanation

Lauren can:

Buy at price 7 (earlier year)
Sell at price 5 (later year)

Loss:

7 - 5 = 2

This is the smallest possible valid loss.

Key Idea

After sorting the prices, the minimum loss will always be found between two neighboring prices in sorted order. Using the original year indices ensures that only valid buy-before-sell transactions are considered. This reduces the solution from O(n²) to O(n log n).
