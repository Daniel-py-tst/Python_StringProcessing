while True:
    fname = input("Enter A File: ")
    try:
        fH = open(fname)
        print(fname, "Found!")
    except:
        print(fname, "Was Not Found.")
        continue
    mode = input("WordCount or WordFilter?: ")
    if mode == "WordCount" or mode == "wordcount":
        HtL = list()
        Hist = dict()
        for line1 in fH:
            line1 = line1.split()
            for word1 in line1:
                Hist[word1] = Hist.get(word1, 0) + 1
        for k,v in Hist.items():
            HtL.append((v,k))
        HtL = sorted(HtL, reverse=True)
        range  = input("Enter Your Desired Range Of Words: ")
        for v,k in HtL[:int(range)]:
            print(v,k)
    elif mode == "WordFilter" or mode == "wordfilter":
        letter = input("Letter(Case Sensitive): ")
        RD = dict()
        for line in fH:
            line = line.split()
            for word in line:
                if word.startswith(letter):
                    RD[word] = RD.get(word, 0) + 1
        for k,v in RD.items():
            print(k)
    rePrompted = input("Would You Like To Process Another File?: ")
    if rePrompted == "Yes" or rePrompted == "yes":
        continue
    else:
        quit()
