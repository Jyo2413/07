import re
input_str = "This is sample string1"
pattern="[i][a-z]" #try different character classes
result = re.findall(pattern, input_str)
print("Matching value", result)




import re
# Define the regular expression for phone numbers
phone_regex = re.compile(r'\+\d{12}')
# Define the regular expression for email addresses
email_regex = re.compile(r'[A-Za-z0-9._]+@[A-Za-z0-9]+\.[A-Z|a-z]{2,}')
# Open the file for reading
with open('example.txt', 'r') as f:
for line in f:
 # Search for phone numbers in the line
 phone_matches = phone_regex.findall(line)
 for match in phone_matches:
 print("Phone Number:", match)
 # Search for email addresses in the line
 email_matches = email_regex.findall(line)
 # Print any email address matches found
 for match in email_matches:
 print("Email Address:", match)
