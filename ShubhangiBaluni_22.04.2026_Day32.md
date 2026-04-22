class Solution {
    public List<List<Integer>> generate(int numRows) {
        List<List<Integer>> triangle = new ArrayList<>();

        for (int i = 0; i < numRows; i++) {
            List<Integer> row = new ArrayList<>();
            // Fill the row
            for (int j = 0; j <= i; j++) {
                // If it's the first or last element of the row, it's 1
                if (j == 0 || j == i) {
                    row.add(1);
                } else {
                    // Sum of two numbers directly above it
                    int leftVal = triangle.get(i - 1).get(j - 1);
                    int rightVal = triangle.get(i - 1).get(j);
                    row.add(leftVal + rightVal);
                }
            }
            triangle.add(row);
        }

        return triangle;
    }
}

URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/22-04-2026.png
