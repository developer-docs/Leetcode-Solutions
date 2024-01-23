class Solution {
    public int maxLength(List<String> arr) {
        List<String> result = new ArrayList<>();
        result.add("");
        for (int i = 0; i < arr.size(); i++) {
            String str = arr.get(i);
            if (!hasUniqueChars(str)) {
                continue;
            }
            List<String> currList = new ArrayList<>();
            for (String s : result) {
                StringBuilder sb = new StringBuilder();
                sb.append(s).append(str);
                if (hasUniqueChars(sb.toString())) {
                    currList.add(sb.toString());
                }
            }
            result.addAll(currList);
        }
        int maxLen = 0;
        for (String str : result) {
            int currLen = str.length();
            if (currLen > maxLen) {
                maxLen = currLen;
            }
        }
        return maxLen;
    }
    private boolean hasUniqueChars(String str) {
        boolean[] visited = new boolean[26];
        for (char ch : str.toCharArray()) {
            if (visited[ch - 'a']) {
                return false;
            }
            else {
                visited[ch - 'a'] = true;
            }
        }
        return true;
    }
}
