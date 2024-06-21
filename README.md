# Technical-Test
TEACH2GIVE TECHNICAL TEST
# Programming Language : Python

# 1.Design a function that reverses the digits of an integer. For example, 50 should become 5 and -12 should become -21.
 Python program to reverse a number 
  
	n = 50
	rev = 0
  
	while(n > 0): 
    a = n % 10
    rev = rev * 10 + a 
    n = n // 10
  
	print(rev)

# 2.Write a recursive function to calculate the factorial of a number.

	def factorial(n): 

	return 1 if (n == 1 or n == 0) else n * factorial(n - 1) 

	num = 5

	print ("Factorial of", num, "is", factorial(num)) 

# 3.Design a function that takes a string or sequence of characters as input and returns the character that appears most frequently.
//Eg 11189 => '1'
//hello => l

	def func(str):
	
 	max=[str[0],str.count(str[0])]
	for i in str:
		if str.count(i)>max[1]:
			max[0]=i 
			max[1]=str.count(i)
  	 return(max)		 

	str="hello"

	print(func(str))

# 4.Design a function that determines whether a given string is a pangram. A pangram is a sentence or phrase containing every letter of the alphabet at least once. Punctuation and case are typically ignored. For example, the string "The quick brown fox jumps over the lazy dog" is a pangram, while "Hello, world!" is not.

	def checkPangram(s):
	
 	List = []
	for i in range(26):
		List.append(False)
	for c in s.lower():
		if not c == " ":
			List[ord(c) - ord('a')] = True
	for ch in List:
		if ch == False:
			return False
	return True
	# Program to test above functions
	sentence = "The quick brown fox jumps over the little lazy dog"

	if (checkPangram(sentence)):
	print('"'+sentence+'"')
	print("\nis a pangram")
	else:
	print('"'+sentence+'"')
	print("\nis not a pangram")

# 5. Design a function that takes a list of integers as input. The function should return True if the list contains two consecutive threes (3 next to a 3) anywhere within the list. Otherwise, it should return False. For example, the function should return True for [1, 3, 3] and False for [1, 3, 1, 3].

	def areConsecutive(arr, n):

	arr.sort()
	for i in range (1,n):
		if(arr[i]!=arr[i-1]+1):
			return False;
			
   	return True; 
    
	arr = [1,3,3]
	n = len(arr)
	if(areConsecutive(arr, n) == True):
	print("Array elements are True ")
	else:
	print("Array elements are False ")

 # 6. Master Yoda, a renowned Jedi Master from the Star Wars universe, is known for his unique way of speaking. He often reverses the order of words in his sentences. For example, instead of saying "I am home" he might say "Home am I" Design a function that takes a sentence as input and returns a newsentence with the words reversed in the same order that Master Yoda would use.
 
	def yoda_speak(sentence):
 	words = sentence.split()
  	reversed_words = words[::-1]
    	yoda_sentence = ' '.join(reversed_words)
    	return yoda_sentence
	# Example
	input_sentence = "I am home"
	yoda_sentence = yoda_speak(input_sentence)
	print(yoda_sentence) 




