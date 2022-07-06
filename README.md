✏擷取文字
====
    #抓【到這裡的文字】
    #參數s是要判斷的字串
    #參數f是從哪擷取start
    #參數b是擷取到哪end
    def get_str_btw(s, f, b): 
        par = s.partition(f) return (par[2].partition(b))[0][:]  
        
    #第一個到》
    tmp_store = tmp[:tmp.index("》")].strip() 

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
