# words_count

import json

if __name__ == '__main__':
    filePATH = "sentences.txt"
    aDict = {}
    with open(filePATH,"r",encoding="utf-8") as f:
        inputLIST = json.load(f)
        for aLine in inputLIST:
            aLineList = aLine.split()
            for ch in aLineList:
                aDict[ch] = aDict.get(ch, 0) + 1
        for keys in aDict:
        print(f"{keys} : {aDict[keys]}")
        
