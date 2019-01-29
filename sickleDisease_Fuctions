aminoAcid = {#create dictionary
    "ATT": "I",
    "ATC": "I",
    "ATA": "I",
    "CTT": "L",
    "CTC": "L",
    "CTA": "L",
    "CTG": "L",
    "TTA": "L",
    "TTG": "L",
    "GTT": "V",
    "GTC": "V",
    "GTA": "V",
    "GTG": "V",
    "TTT": "F",
    "TTC": "F",
    "ATG": "M"
    }
dnaInput = input("What is the DNA sequance?: ").upper()#get user input
dna_list = [dnaInput[i:i+3] for i in range(0,len(dnaInput),3)]#change data input into array of 3
print(dna_list)

def translate():#function to compare user input to dictionary value
    
    for key, value in aminoAcid.items():#for loop to get information from dictionary
        for dna in dna_list:
            if dna == key:#if statement to compare input to dictionary
                if value == "I":
                    print("The DNA conone " + dna + " corresponding Amino Acids is: Isoleucine")
                elif value == "L":
                    print("The DNA conone " + dna + " corresponding Amino Acids is: Leucine")
                elif value == "V":
                    print("The DNA conone " + dna + " corresponding Amino Acids is: Valine")
                elif value == "F":
                    print("The DNA conone " + dna + " corresponding Amino Acids is: Phenylalanine")
                elif value == "M":
                    print("The DNA conone " + dna + " corresponding Amino Acids is: Methionine")
                else:
                    print("The DNA conone " + dna + " corresponding Amino Acids is: X")
                
           
translate()#call of function

def mutate():#function to mutate text file
    f = open('DNA.txt', 'r')#open text file
    nf1 = open('normalDNA.txt','w')#create txt file to write to
    nf2 = open('mutatedDNA.txt','w')#create txt file to write to
    for line in f:#for loop to read through txt file.
        data = line.upper()#change to data
        data2 = line.replace('a', 'T')#replace a with T
        nf1.write(data)#write to file
        nf2.write(data2)#write to file

mutate()#call function

def txtTranslate():#function to call txt file and compare to dictionary
    nD = open('normalDNA.txt', 'r')
    mD = open('mutatedDNA.txt', 'r')

    for nline in nD:
         nd_list = [nline[i:i+3] for i in range(0,len(nline),3)]#change list to array with each unit only3

 
    for mline in mD:
         md_list = [mline[i:i+3] for i in range(0,len(mline),3)]#change list to array with each unit only3


    for key, value in aminoAcid.items():#for loop to get value from dictionary
        for nDNA in nd_list:
            if nDNA == key:#if statement to compare txt file to dictionary
                if value == "I":
                    print("The DNA conone " + nDNA + " in normalDNA.txt corresponding Amino Acids is: Isoleucine")
                elif value == "L":
                    print("The DNA conone " + nDNA + " in normalDNA.txt corresponding Amino Acids is: Leucine")
                elif value == "V":
                    print("The DNA conone " + nDNA + " in normalDNA.txt corresponding Amino Acids is: Valine")
                elif value == "F":
                    print("The DNA conone " + nDNA + " in normalDNA.txt corresponding Amino Acids is: Phenylalanine")
                elif value == "M":
                    print("The DNA conone " + nDNA + " in normalDNA.txt corresponding Amino Acids is: Methionine")
                else:
                    print("The DNA conone " + nDNA + " in normalDNA.txt corresponding Amino Acids is: X")

    for key, value in aminoAcid.items():#for loop to get value from dictionary
        for mDNA in md_list:
            if mDNA == key:#if statement to compare txt file to dictionary
                if value == "I":
                    print("The DNA conone " + mDNA + " in mutatedDNA.txt corresponding Amino Acids is: Isoleucine")
                elif value == "L":
                    print("The DNA conone " + mDNA + " in mutatedDNA.txt corresponding Amino Acids is: Leucine")
                elif value == "V":
                    print("The DNA conone " + mDNA + " in mutatedDNA.txt corresponding Amino Acids is: Valine")
                elif value == "F":
                    print("The DNA conone " + mDNA + " in mutatedDNA.txt corresponding Amino Acids is: Phenylalanine")
                elif value == "M":
                    print("The DNA conone " + mDNA + " in mutatedDNA.txt corresponding Amino Acids is: Methionine")
                else:
                    print("The DNA conone " + mDNA + " in mutatedDNA.txt corresponding Amino Acids is: X")
            

txtTranslate()#call of function
