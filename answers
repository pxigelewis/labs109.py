#QESTION 1

def ryerson_letter_grade(pct):

    grade = pct
    
    if grade >= 90 and grade <= 150:
        return ('A+')
    elif grade >= 85 and grade <= 89:
        return ('A')
    elif grade >= 80 and grade <= 84:
        return ('A-')
    elif grade >= 77 and grade <= 79:
        return ('B+') 
    elif grade >= 73 and grade <= 76:
        return ('B')
    elif grade >= 70 and grade <= 72:
        return ('B-')
    elif grade >= 67 and grade <= 69:
        return ('C+')
    elif grade >= 63 and grade <= 66:
        return ('C')
    elif grade >= 60 and grade <= 62:
        return ('C-')
    elif grade >= 57 and grade <= 59:
        return ('D+') 
    elif grade >= 53 and grade <= 56:
        return ('D')
    elif grade >= 50 and grade <= 52:
        return ('D-')
    elif grade >= 0 and grade <= 49:
        return ('F')



#QUESTION 2    

def is_ascending(items):
    is_asc = True
    for x in range(len(items) - 1):
        t = items[x+1] - items[x]
        if not t > 0:
            is_asc = False
            break
    return is_asc
           
              

#QUESTION 3

list1 = []

def  only_odd_digits(n):
    digits = [int(i) for i in str(n)]                         
    ans = True
    for digit in digits:
        if digit % 2 == 0 or digit == 0:                         
            ans = False
            break
    return ans



#QUESTION 4
    
def prime_factors(n): 
    primfac = []
    d = 2
    while d*d <= n:
        while (n % d) == 0:
            primfac.append(d)
            n //= d
        d += 1
    if n > 1:
           primfac.append(n)
    return primfac



#QUESTION 5
    
def first_missing_positive(items):
    if not items:
        return 1
    for index, value in enumerate(items):
        if len(items) < value <= 0:
            continue
        while index + 1 != items[index] and 0 < items[index] <= len(items):
            v = items[index]
            items[index], items[v-1] = items[v-1], items[index]
            items[v-1] = v
            if items[index] == items[v-1]:
                break
    for index, value in enumerate(items, 1):
        if value != index:
            return index
    return len(items) + 1



#QUESTION 6
    
def is_permutation(items, n):
    counter = [0]*len(items)
    limit = len(items)
    for element in items:
        if not 1 <= element <= limit:
            return False
        else:
            if counter[element-1] != 0:
                return False
            else:
                counter[element-1] = 1
    return True



#QUESTION 7
    
def hand_is_badugi(hand):
    card = []
    suit = []
    for i, j in hand:
        card.append(i)
        suit.append(j)
    cardset = list(set(card))
    suitset = list(set(suit))
    if len(card) == len(cardset) and len(suit) == len(suitset):
        return True
    else:
        return False

        
    
#QUESTION 8
        
def group_equal(items):
    groups = []
    for item in items:
        if len(groups) == 0:
            groups.append([item])
        elif item == groups[-1][0]:
            groups[-1].append(item)
        else:
            groups.append([item])
    return groups



#QUESTION 9
        
def running_median_of_three(items):
    import statistics
    med = []
    firsttwoitems = items[0:2]
    if len(items) <= 2:
        return items
    if len(items) > 2:
        for i in range(len(items)):
            med.append(statistics.median(items[i:i+3]))
            x = firsttwoitems + med
        return x[:-2]
    
    
    
#QUESTION 10

def collapse_intervals(items):
    prev = min(items) if items else None
    n = list()
    for num in sorted(items):
        if num != prev+1:
            n.append([num])
        elif len(n[-1]) > 1:
            n[-1][-1] = num
        else:
            n[-1].append(num)
        prev = num
    return ','.join(['-'.join(map(str, list_item)) for list_item in n])



#QUESTION 11
    
def reverse_reversed(items):
    if isinstance(items, list):
        return list(reverse_reversed(x) for x in reversed(items))
    else:
        return items
    
    
    
#QUESTION 12
        
def count_carries(a, b):
    func = lambda n:sum(map(int,str(n)));
    return int((func(a) + func(b) -func(a+b)) / 9)



#QUESTION 13
    
def count_and_say(digits):
    if len(digits) == 0:
        return ""
    else:
        result = ""
        ch = digits[0]
        count = 1
        for digit in digits[1:]:
            if digit == ch:
                count += 1
            else:
                result += str(count)
                result += ch
                count = 1
            ch = digit
        result += str(count)
        result += ch
        return result



#QUESTION 14
    
def create_zigzag(rows, cols, start=1):
    grid = []
    for row in range(rows):
        begin = start + row * cols
        end = begin + cols
        r = list(range(begin, end))
        grid.append(r if row % 2 == 0 else r[::-1])
    return grid



#QUESTION 15

def all_cyclic_shifts(text):
    i = 0
    j = list(text)
    result = []
    while i < len(j):
        j.append(j.pop(0))           
        k = "".join(j)
        result.append(k)
        i+=1
    return sorted(list(set(result)))



#QUESTION 16
    
def count_consecutive_summers(n):
    ans = 0
    for i in range(1, 2*n + 1):
        if 2*n % i == 0:
            y = 2 * n / i - i - 1
            if y % 2 == 0 and y >= 0:
                ans += 1
    return ans



#QUESTION 17
    
def expand_intervals(intervals):
    items = intervals.split(",")
    ans = []
    for item in items:
        item = item.strip()
        if "-" in item:
            a = int(item.split("-")[0])
            b = int(item.split("-")[1])
            for i in range(a, b + 1):
                ans.append(i)
        else:
            ans.append(int(item))
    return ans



#QUESTION 18

def is_perfect_power(n):
    x = 2
    while True:
        if 2 ** x > n: 
            return False
        a = 2
        b = a
        while b ** x <= n:
            b *= 2
        while b - a > 1:
            mid = (a + b) // 2
            if mid ** x <= n:
                a = mid
            else:
                b = mid
        if a ** x == n:
            return True
        x += 1
        
        

#QUESTION 19

#def fibonacci_sum(n):
#    first = 0
#    second = 1
#    fib_list = []
#    values = []
#    fib_list.append(first)
#    fib_list.append(second)
#    next = first + second
#    while next <= n:
#        fib_list.append(next)
#        first = second
#        second = next
#        next = first + second
#    answer = 0
#    fib_list.sort(reverse=True)
#    while True:
#        for i in fib_list:
#            if answer + i > n:
#                continue
#            else:
#                values.append(i)
#                answer = answer + i
#                if answer == n:
#                    break
#                fib_list.remove(i)
#        if answer == n:
#            break
#
#    return values


#QUESTION 20
        
def safe_squares_rooks(n, rooks):
    unsafer = set() #unsafe rows
    unsafec = set() #unsafe columns
    for i in rooks:
        unsafer.add(i[0])
        unsafec.add(i[1])
    src = n -len(unsafer)
    scc = n -len(unsafec)
    safe = src * scc
    return safe
    
    

#QUESTION 21
    
def double_until_all_digits(n, giveup = 1000):
    for i in range(giveup):
        if set(list('0123456789')).issubset(list(str(n))):
            return i
        n *= 2
    return -1



#QUESTION 22
    
def frequency_sort(elms):
    from collections import Counter
    counts = Counter(elms)
    newlst = sorted(counts.most_common(), key=lambda a: (-a[1], a[0]))
    sublst = [([b]*n) for (b,n) in newlst]
    return[item for sublist in sublst for item in sublist]
    


#QUESTION 23
    
def reverse_ascending_sublists(items):
    ans = []
    sublst = []
    for item in items:
        if len(sublst) == 0:
            sublst.append(item)
        else:
            if item > sublst[0]:
                sublst.insert(0, item)
            else:
                ans.extend(sublst)
                sublst = [item]
    ans.extend(sublst)
    return ans
    


#QUESTION 24
    
def bridge_hand_shape(hand):
    cards = []
    dist = []
    for a, b in hand:
        cards.append(b)
    s = cards.count('spades')
    dist.append(s)
    h = cards.count('hearts')
    dist.append(h)
    d = cards.count('diamonds')
    dist.append(d)
    c = cards.count('clubs')
    dist.append(c)
    return dist
    


#QUESTION 25
    
def longest_palindrome(text):
    ans = []
    if len(text) == 1:
        return text
    for i in range(1,len(text)):
        texta, textb = text[:i][::-1], text[i:]
        s1 = string_match(texta, textb)
        s1 = s1[::-1] + s1
        s2 = string_match(texta, textb[1:])
        s2 = s2[::-1] + textb[0] + s2
        ans.append(s1)
        ans.append(s2)
    m = max([len(i) for i in ans])
    if m==1:
        return text[0]
    else:
        return [i for i in ans if len(i)==m][0]
    
def string_match(stringa, stringb):
    ans = []
    for i in range(min(len(stringa), len(stringb))):
        if stringa[i] == stringb[i]:
            ans.append(stringb[i])
        else:
            break
    return ''.join(ans)
    
    

#QUESTION 26
    
def iterated_remove_pairs(items):
    a = 0
    previous = None
    while a < len(items):
        number = items[a]
        if number == previous:
            items.pop(a)
            items.pop(a-1)
            a -= 1
        else:
            a +=1
        if a:
            previous = items[a-1]
        else:
            previous = None
    return items



#QUESTION 27
    
def disemvowel(text):
    s = text
    v = ["a", "e", "i", "o", "u"]
    sw  =  s.replace("ay",  "a").replace("ya",  "a").replace("ye",  "e").replace("ey",  "e").replace("yi", "i").replace("iy", "i").replace("yo", "o").replace("oy", "o").replace("uy", "u").replace("yu", "u")
    return "".join([i for i in sw if i not in v])



#QUESTION 28
    
def detab(text, n = 8, sub = ' '):
    word = n*sub
    return''.join([i.replace("\t",word) for i in text])
    
    
    
#question 29
    
def postfix_evaluate(items):
    stack = []
    for item in items:
        if type(item) is int:
            stack.append(item)
            continue
        num1, num2 = stack.pop(), stack.pop()
        if item == '+':
            stack.append(num2 + num1)
        elif item == '-':
            stack.append(num2 - num1)
        elif item == '*':
            stack.append(num2 * num1)
        elif item == '/':
            if num1!=0:
                stack.append(num2 // num1)
            else:
                stack.append(0)
    return stack.pop()



#QUESTION 30
    
def squares_intersect(s1, s2):
    square1x1 = s1[0]
    square1y1 = s1[1]
    square1x2 = square1x1 + s1[2]
    square1y2 = square1y1 + s1[2]

    square2x1 = s2[0]
    square2y1 = s2[1]
    square2x2 = square2x1 + s2[2]
    square2y2 = square2y1 + s2[2]

    if square1x2 < square2x1 or square2x2 < square1x1:
        return False
    if square1y2 < square2y1 or square2y2 < square1y1:
        return False
    return True


            
#QUESTION 31
    
def maximum_difference_sublist(items, k = 2):
    difference = 0
    l = []
    for i in range(len(items)-k+1):
        d = 0
        t = items[i:i+k]
        d = max(t) - min(t)
        if difference < d or len(l) == 0:
            difference = d
            l = items[i:i+k]
    return l
