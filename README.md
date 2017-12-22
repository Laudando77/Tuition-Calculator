# Tuition-Calculator

# MBA/MS Tuition calculator 12/19/17 Christopher Laudando
 
# Fee definitions
AEF = 1000 # Academic Excellence Fee 12 or more credits

PTAEF = 750 # Academic Excellence Fee less than 12 credits

FT_Tech_fee = 125 # Technology Fee 12 or more credits

PT_Tech_fee = 62.50 # Technology Fee less than 12 credits

confee = 15 # Consolidated Services Fee

ActFee = 39.60 # Activity Fee

SummerFee = 14.45 # Summer Activity Fee OYMBA 

# Tuition definitions 
MBA_PT_NY = 685 # MBA Tuition PT per credit NY Resident

MBA_NON_NY = 1050 # MBA Tuition per credit NON Resident

MBA_FT_NY = 7685 # MBA Tuition FT per term NY Resident

MS_FT_NY = 5225 # MS Tuition per term NY Resident

MS_PT_NY = 440 # MS Tuition PT per credit NY Resident

MS_NON_NY = 805 # MS Tuition per credit NON Resident



# welcome message
print("Welcome to the Zicklin School of Business Tuition Calculator! \n")
print("Calculate your first year's total tuition and fees costs for Evening MBA/Full-Time MBA/One-Year MBA or MS program tuition. \n")

print("Note: All tuition and fees are subject to change without notice. \n")
# full time part time

print("Attending Type:")
print("1. Full-Time (12 or more credits)")
print("2. Part-Time (less than 12 credits)")

at = input("Enter choice 1 or 2:")

# residency
print("Your Residency Status:")
print("1. New York State resident")
print("2. Non-Resident")

res = input("Enter choice 1 or 2:")

# program type

print("Enter Graduate Program Type:")
print("1. Evening MBA or Full-Time MBA")
print("2. One-Year MBA")
print("3. MS")
prog = input("Enter 1 or 2 or 3:")

# number of credits
print("How many credits will you be taking this semester?")

i = int(input())

# full time scenarios IN STATE

if at == '1' and prog == '1' and res == '1' and i in range(12, 19):
   print('Academic Excellence Fee: $' + str(AEF)+ ' (12 or more credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(FT_Tech_fee)+ ' per semester (full-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $8864.60 per term.')

elif at == '1' and prog == '3' and res == '1'and i in range(12, 19):
   print('Academic Excellence Fee: $' + str(AEF)+ ' (12 or more credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(FT_Tech_fee)+ ' per semester (full-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $6404.60 per term.')

# full time scenarios OUT OF STATE
elif at == '1' and prog == '3' and res == '2'and i in range(12, 19):
   print('Academic Excellence Fee: $' + str(AEF)+ ' (12 or more credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(FT_Tech_fee)+ ' per semester (full-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $' + str(int(i) * MS_NON_NY+AEF+FT_Tech_fee+confee+ActFee) + ' per term.')    

elif at == '1' and prog == '1' and res == '2'and i in range(12, 19):
   print('Academic Excellence Fee: $' + str(AEF)+ ' (12 or more credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(FT_Tech_fee)+ ' per semester (full-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $' + str(int(i) * MBA_NON_NY+AEF+FT_Tech_fee+confee+ActFee) + ' per term.') 

# part time scenarios IN STATE   
elif at == '2' and prog == '1' and res == '1'and i < 12:
   print('Academic Excellence Fee: $' + str(PTAEF)+ ' (Less than 12 credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(PT_Tech_fee)+ 'per semester (part-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $' + str(int(i) * MBA_PT_NY+PTAEF+PT_Tech_fee+ActFee+confee) + ' per term.')

elif at == '2' and prog == '3' and res == '1'and i < 12:
   print('Academic Excellence Fee: $' + str(PTAEF)+ ' (Less than 12 credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(PT_Tech_fee)+ ' per semester (part-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $' + str(int(i) * MS_PT_NY+PTAEF+PT_Tech_fee+ActFee+confee) + ' per term.')

# part time scenarios OUT OF STATE
elif at == '2' and prog == '1' and res == '2'and i < 12:
   print('Academic Excellence Fee: $' + str(PTAEF)+ ' (Less than 12 credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(PT_Tech_fee)+ 'per semester (part-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $' + str(int(i) * MBA_NON_NY+PTAEF+PT_Tech_fee+ActFee+confee) + ' per term.')

elif at == '2' and prog == '3' and res == '2'and i < 12:
   print('Academic Excellence Fee: $' + str(PTAEF)+ ' (Less than 12 credits).')
   print('Activities Fee: $' + str(ActFee)+ ' per Fall & Spring term.')
   print('Technology Fee: $' + str(PT_Tech_fee)+ ' per semester (part-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $' + str(int(i) * MS_NON_NY+PTAEF+PT_Tech_fee+ActFee+confee) + ' per term.')

# One-Year MBA 
elif at == '1' and prog == '2' and res == '1' and i == 18:
   print('Activities Fee: $' + str(SummerFee)+ ' Summer entry term.')
   print('Technology Fee: $' + str(FT_Tech_fee)+ ' per semester (full-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees: $12484.45 Summer term (18 credits).')

elif at == '1' and prog == '2' and res == '2'and i == 18:
   print('Activities Fee: $' + str(SummerFee)+ ' Summer entry term.')
   print('Technology Fee: $' + str(FT_Tech_fee)+ ' per semester (full-time students).')
   print('Consolidated Services Fee: $' + str(confee) + ' per term.')
   print('Total Tuition and Fees Summer: $19054.45 Summer term (18 credits).')

else:
   print('Invalid Entry')
