class Solution {
    public String mostCommonWord(String paragraph, String[] banned) {
        paragraph += ".";

        Set<String> set = new HashSet();
        for (String word: banned) set.add(word);
        Map<String, Integer> map = new HashMap();

        String ans = "";
        int ansfreq = 0;

        StringBuilder word = new StringBuilder();
        for (char c: paragraph.toCharArray()) {
            if (Character.isLetter(c)) {
                word.append(Character.toLowerCase(c));
            } else if (word.length() > 0) {
                String finalword = word.toString();
                if (!set.contains(finalword)) {
                    map.put(finalword, map.getOrDefault(finalword, 0) + 1);
                    if (map.get(finalword) > ansfreq) {
                        ans = finalword;
                        ansfreq = map.get(finalword);
                    }
                }
                word = new StringBuilder();
            }
        }

        return ans;
    }
}
