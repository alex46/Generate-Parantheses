Generate-Parantheses
====================

    public class Solution {
    ArrayList<String> result;
    public ArrayList<String> generateParenthesis(int n) {
    // Start typing your Java solution below
    // DO NOT write main() function
    result = new ArrayList<String>();
    if (n<1) return result;
    addBrackets(new String(""), n, 0, 0);
    return result;
    }
    private void addBrackets(String str, int target, int open, int close) {
    if (close == target) {
    result.add(str);
    }
    else {
    if (open > close) {
    addBrackets(str + ")", target, open, close + 1);
    }
    if (open < target) {
    addBrackets(str + "(", target, open + 1, close);
    }
    }
    }
    }
