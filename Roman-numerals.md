Given a positive integer number less than 4000 (eg 42) determine its Roman numeral representation as a String (eg "XLII").<br>
<br>
You cannot write numerals like IM for 999. Wikipedia states "Modern Roman numerals are written by expressing each digit separately starting with the leftmost digit and skipping any digit with a value of zero."<br>
<br>
Examples:<br>
<br>
1 ->    "I" | 10 ->    "X" | 100 ->    "C" | 1000 ->    "M"<br>
2 ->   "II" | 20 ->   "XX" | 200 ->   "CC" | 2000 ->   "MM"<br>
3 ->  "III" | 30 ->  "XXX" | 300 ->  "CCC" | 3000 ->  "MMM"<br>
4 ->   "IV" | 40 ->   "XL" | 400 ->   "CD" |<br>
5 ->    "V" | 50 ->    "L" | 500 ->    "D" |<br>
6 ->   "VI" | 60 ->   "LX" | 600 ->   "DC" |<br>
7 ->  "VII" | 70 ->  "LXX" | 700 ->  "DCC" |<br>
8 -> "VIII" | 80 -> "LXXX" | 800 -> "DCCC" |<br>
9 ->   "IX" | 90 ->   "XC" | 900 ->   "CM" |<br>
<br>
1990 -> "MCMXC"  (1000 -> "M"  + 900 -> "CM" + 90 -> "XC")<br>
2008 -> "MMVIII" (2000 -> "MM" + 8 -> "VIII")<br>
  99 -> "XCIX"   (90 -> "XC" + 9 -> "IX")<br>
  47 -> "XLVII"  (40 -> "XL" + 7 -> "VII")<br>
3888 -> "MMMDCCCLXXXVIII" (3000 -> "MMM" + 800 -> "DCCC" + 80 -> "LXXX" + 8 -> "VIII")