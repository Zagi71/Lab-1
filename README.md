# Lab-1
Counting nucleotides
#!/usr/bin/env python3
# Name: Zargham
# Group Members: Aanand Verna, Andrew Matsiev, Rogelio Chavez, Samuel Hirsch
# in this program you can plug in any sequence and it will give you all number of all the letters
class dnaString (str):
    def length (self):
        return (len(self))

    def getAT (self):
      #we will write A as string
        num_A = self.count("A")
        num_T = self.count("T")
        #we will call length function
        return ((num_A + num_T)/ self.length() )
    def countNucleotideA (self):
      #This will count accurence of A
        num_A = self.count('A')
        return num_A
    #This will count accurence of C
    def countNucleotideC (self):
        num_C = self.count('C')
        return num_C
    #This will count accurence of G
    def countNucleotideG (self):
        num_G = self.count('G')
        return num_G
    #This will count accurence of T
    def countNucleotideT (self):
        num_T = self.count('T')
        return num_T
#INPUT THE DNA SEQUENCE
dna = input("Enter a dna sequence: ")
#CONVERT TO UPPER CASE
upperDNA = dna.upper()
#CREATING OBJECT FOR THAT SPECCIFIC SEQUENCE
coolString = dnaString(upperDNA)
#PRINT TIME OF A,C,G,T
print ("number As = {} number C = {} number Gs = {} number T = {}".format(
    coolString.countNucleotideA(),
    coolString.countNucleotideC(),coolString.countNucleotideG(),
    coolString.countNucleotideT()))
