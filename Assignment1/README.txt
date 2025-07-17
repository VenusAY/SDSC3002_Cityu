Au-Yeung Fung Yin
57269800

First, a class named as Apriori

for the initial parts,

variable file, store the file name "trans.txt"
transection initialize as empty list to store the transection in the trans.txt file
trans_dict = defaultdict(int)
C_itemset = defaultdict(int) 
# k-item set for the item in dict format

GlobalFreqItem = {}
K(start at 1)

I create 5 function of the class, LoadData, Candidate_Generation, Count_Support, freq_item_dict, and the main aporior algothrim.

def LoadData(self):
        with open(self.file,'r') as file:
            data = file.readlines()
            for i in data:
                temp = frozenset(map(int,i.split()))
                self.transection.append(temp) 
            
                for item in temp:
                    self.C_itemset[frozenset([item])] +=1

transform the data into set format and append to the transection list.
C_itemset is storing the no. of elements 
                   

def Candidate_Generation(self,prev_freq_items):
        
		return set().union(*prev_freq_items)         
 use to combine the frozenset       
    

    def Count_Support(self,transection, k):
        C_support = defaultdict(int)
        for i in transection:
            if len(i) == k:
                    C_support[i]+=1
            
            elif len(i)>k:
                for j in [combinations(i,k)]:
                    if frozenset(j).issubset(i):
                            C_support[frozenset(j)]+=1
        return C_support
    
    def freq_item_dict(self, item_dict, support):
        
        return {k:v for k,v in item_dict.items() if v >= support}
        
    
     
    
    def apriori(self, minFreq):
        time_start = datetime.now()
        self.LoadData()
    
        minSup = minFreq * len(self.transection)
 
        prev_freq_items = self.freq_item_dict(self.C_itemset, minSup)
        while len(prev_freq_items) > 0:
            candidates = self.Candidate_Generation(prev_freq_items.keys())
            C_k = self.Count_Support(self.transection, self.K+1 )
            prev_freq_items = self.freq_item_dict(C_k, minSup)
            self.GlobalFreqItem[self.K] = prev_freq_items
            self.K += 1



            
        
        time = datetime.now() - time_start
    
        return self.GlobalFreqItem, time



Min Support: 0.0001
lv 1
no.of freq element 733

lv 2
no.of freq element 8133

lv 3
no.of freq element 7998

lv 4
no.of freq element 1740

lv 5
no.of freq element 90

lv 6
no.of freq element 0

Time using: 0:01:13.798359


Min Support: 0.0002
lv 1
no.of freq element 592

lv 2
no.of freq element 4553

lv 3
no.of freq element 2734

lv 4
no.of freq element 334

lv 5
no.of freq element 6

lv 6
no.of freq element 0

Time using: 0:00:35.220623


Min Support: 0.0003
lv 1
no.of freq element 524

lv 2
no.of freq element 3081

lv 3
no.of freq element 1342

lv 4
no.of freq element 129

lv 5
no.of freq element 1

lv 6
no.of freq element 0

Time using: 0:00:27.730826


Min Support: 0.0004
lv 1
no.of freq element 470

lv 2
no.of freq element 2237

lv 3
no.of freq element 800

lv 4
no.of freq element 49

lv 5
no.of freq element 0

Time using: 0:00:19.982686


Min Support: 0.0005
lv 1
no.of freq element 437

lv 2
no.of freq element 1727

lv 3
no.of freq element 505

lv 4
no.of freq element 26

lv 5
no.of freq element 0

Time using: 0:00:18.363135
