✏查看 Python版本
====
    python —version

✏查看 Pytorch版本
====
    python 
    import torch
    print(torch.**version**)
    👋ctrl+z 或者exit
out：1.11.0+cpu

✏擷取文字-函式
====
    #抓【到這裡的文字】
    #參數s是要判斷的字串
    #參數f是從哪擷取start
    #參數b是擷取到哪end
    def get_str_btw(s, f, b): 
        par = s.partition(f) return (par[2].partition(b))[0][:]  
        
    #第一個到》
    tmp_store = tmp[:tmp.index("》")].strip() 

✏擷取文字-index
====
    str1 = "HELLO . WORLD"
    str2 = "."
    print(:str1.index(str2))      #印出 "HELLO"
    print(str1.index(str2):)      #印出 "WORLD"

✏擷取數字
====
    import re    #導入正規運算式
    變數 = re.findall(r"\d",字串)

✏文字的相似度判斷
===
    #相似度函式
    #如果某店家之資料表內的所有資料與要新增進去的資料相比
    #相似度大於等於0.5就視為同個優惠 
    def similarity(a, b): 
         return SequenceMatcher(None, a, b).ratio() 

✏資料夾內最新的那個檔案之讀取
===
    #找出最新一筆檔案(依據最後更動時間)#用來判斷儲存最後一次的id
    #下次才知道id從多少開始
    #而檔名是依據日期去建立的
    def new_report(test_report): 
       #列出目錄的下所有文件和文件夾保存到
        lists lists = os.listdir(test_report) 
        #按時間排序 
        lists.sort(key=lambda fn:os.path.getmtime(test_report + "\\" + fn)) 
        #獲取最新的文件保存到file_new  
        file_new = os.path.join(test_report,lists[-1]) 
    return file_new
    
✏額外將結果輸出至記事本
====
    tp = 1
    path = 'want.txt'
    all_thing = "tp" + str(tp)
    f = open(path,'a')
    f.write(all_thing)
    f.close()

✏取代記事本文字內的資料
====
        #要修改內容的記事本
        path = "test.txt"
        f = open(path,'r')

        #修改路徑從 darknetYolo 移至 yolov7-wang 中
        ssa = "D:/darknetYolo/darknet/build/darknet/x64/yolov4/LabelmeData/tmp/SSA_all"
        ta = "D:/darknetYolo/darknet/build/darknet/x64/yolov4/LabelmeData/tmp/TA_all"
        hp = "D:/darknetYolo/darknet/build/darknet/x64/yolov4/LabelmeData/tmp/HP_all"
        new = "D:/desktop/yolov7-wang/data/image"
        replacement = ""

        #將取代後的文字都塞到字串 replacement 中
        for line in f:
            line = line.strip()
            if ssa in line:
                change = line.replace(ssa,new)
                replacement = replacement + change + "\n"

            elif ta in line:
                change = line.replace(ta,new)
                replacement = replacement + change + "\n"

            elif hp in line:
                change = line.replace(hp,new)
                replacement = replacement + change + "\n"

        f.close()

        #打開記事本並寫入
        fout = open("test.txt","w")
        fout.write(replacement)
        fout.close()

✏程式碼漂亮技巧-分割線/太長要切割
====
1.輸入 "#%%" 井趴趴
=>將出現如圖的直線
![image](https://user-images.githubusercontent.com/46515944/177496418-b0644aa6-dfa3-4e34-a56b-112d5dd8cccd.png)


2.一條程式碼太長
輸入 "\" 斜線 =>如圖

![image](https://user-images.githubusercontent.com/46515944/177496439-939f0457-3fe3-437a-977b-7928c16fdff7.png)

✏Colab 可愛小分享
===
![image](https://user-images.githubusercontent.com/46515944/177496813-34120a7d-ab98-4fde-93b5-3af2eb00c093.png)
1. 首先開啟你的colab
2. 在畫面右上角你自己google帳號的那個圓圈旁邊，有一個像設定符號的按鈕，給他按下去
![image](https://user-images.githubusercontent.com/46515944/177497022-1bc96b95-96cd-4e7b-b14b-da66d6d358f7.png)
3. 接著看到如下圖的畫面後，點選"其他"

![image](https://user-images.githubusercontent.com/46515944/177496969-9cfc4a94-bc49-400e-b9ae-b42ae13947fb.png)

4. 最後看你是狗派還是貓派，勾選你喜歡的模式吧

![image](https://user-images.githubusercontent.com/46515944/177496932-eca25d6b-299a-40d4-afb5-2f14d75e624f.png)

🌱附註：如果你兩個都愛的話，恭喜你可以複選!!

🌱附註：效能等級那裏可以玩玩看

⚠暴雷：效能等級點"Many Power"的話，每打一個字就會有遊戲的蹦蹦效果，如下圖這個東東
