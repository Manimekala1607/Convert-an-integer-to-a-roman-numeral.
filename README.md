# Convert-an-integer-to-a-roman-numeral.
class RomanSolution:
    @staticmethod
    def int_to_roman(num):
        val = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1]
        syb = ["M", "CM", "D", "CD", "C", "XC", "L", "XL",
               "X", "IX", "V", "IV", "I"]
            if num < 1 or num > 3999:
            return "ENTER A GOOD VALUE!"
        roman_num = ""
        i = 0
        while num > 0:
            if num >= val[i]:
                roman_num += syb[i]
                num -= val[i]
            else:
                i += 1
        return roman_num
n = int(input("ENTER A NUMBER: "))
print("Roman numeral of given number is:", RomanSolution.int_to_roman(n))

OUTPUT 1:
ENTER A NUMBER: 9876
Roman numeral of given number is: ENTER A GOOD VALUE!
OUTPUT 2:
ENTER A NUMBER: 2510
Roman numeral of given number is: MMDX


