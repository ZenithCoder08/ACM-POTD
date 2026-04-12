class Solution {
    public int[][] floodFill(int[][] image, int sr, int sc, int color) {
        int originalColor = image[sr][sc];
        
        // If the starting pixel is already the target color, no work needed
        if (originalColor != color) {
            dfs(image, sr, sc, originalColor, color);
        }
        
        return image;
    }

    private void dfs(int[][] image, int r, int c, int originalColor, int newColor) {
        // Check bounds and if the current pixel matches the original color
        if (r < 0 || r >= image.length || c < 0 || c >= image[0].length || image[r][c] != originalColor) {
            return;
        }

        // Update the color
        image[r][c] = newColor;

        // Spread to neighbors
        dfs(image, r + 1, c, originalColor, newColor); // Down
        dfs(image, r - 1, c, originalColor, newColor); // Up
        dfs(image, r, c + 1, originalColor, newColor); // Right
        dfs(image, r, c - 1, originalColor, newColor); // Left
    }

    URL : https://github.com/ZenithCoder08/ACM-POTD/blob/main/12-04-2026.png
}
